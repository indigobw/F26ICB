#Directory
data_dir <- "C:/Users/VivaA/2214/IntroBiolComp-2026/R/DataFiles/Saavedra2013/"

#List files
files <- list.files(
  path = data_dir,
  pattern = "\\.txt$",
  full.names = TRUE
)

#Data storage
Data <- data.frame(
  File = character(),
  Nrow = integer(),
  Ncol = integer(),
  p_1 = numeric(),
  p_0 = numeric(),
  stringsAsFactors = FALSE
)

#Check files
class(files)
str(files)
print(files)

#Sort files
for (f in files) {
  mat <- read.table(f, header = FALSE)
  Data <- rbind(
    Data,
    data.frame(
      File = basename(f),
      Nrow = nrow(mat),
      Ncol = ncol(mat),
      p_1 = mean(as.matrix(mat) == 1),
      p_0 = mean(as.matrix(mat) == 0)
    )
  )
}

#Write results
write.table(
  Data,
  file = "MatrixStats.tsv",
  sep = "\t",
  row.names = FALSE,
  quote = FALSE
)

head(Data)



#Installing BiocManager
if (!require("BiocManager", quietly = TRUE))
  install.packages("BiocManager")

BiocManager::install("EBImage")

library(EBImage)

#Directory and files
data_dir <- "C:/Users/VivaA/2214/IntroBiolComp-2026/R/DataFiles/leafarea/"
source(file.path(data_dir, "getArea.R"))
files <- list.files(
  path = data_dir,
  pattern = "\\.JPG$",
  full.names = TRUE,
  ignore.case = TRUE,
)
length(files)

#Loop images and get area
image_results <- data.frame(
  filename = basename(files),
  area = numeric(length(files)),
  stringsAsFactors = FALSE
)
for (i in seq_along(files)) {
  image_results$area[i] <- getArea(files[i])
}
head(image_results)

#Had to get the EBImage to work
library(EBImage)

#Data formatting - I looked this up, the method I was using wasn't working
image_results$timepoint <- sub(
  "^([^_]+)_.*$", "\\1", image_results$filename
)
image_results$plant <- sub(
  "^[^_]+_(.*)\\.JPG$", "\\1",
  image_results$filename,
  ignore.case = TRUE
)
results <- reshape(
  image_results[, c("plant", "timepoint", "area")],
  idvar = "plant",
  timevar = "timepoint",
  direction = "wide"
)

#Leaf area change
results$change_area <- results$area.t2 - results$area.t1
average_growth <- mean(results$change_area, na.rm = TRUE)
print(results)
cat("Average leaf area growth:", average_growth, "pixels\n")

#Save results
write.csv(
  results,
  file = file.path(data_dir, "leaf_area_results.csv"),
  row.names = FALSE
head(results)