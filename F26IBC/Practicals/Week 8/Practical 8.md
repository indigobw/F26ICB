Practical 8
#Reading file
geno <- read.table("C:/Users/VivaA/2214/IntroBiolComp-2026/R/Datafiles/H938_Euro_chr6.geno", sep=" ", h=T)
str(geno)
#Getting numbers
geno$A1 <- as.factor(geno$A1)
geno#A2 <- as.factor(geno$S2)
head(geno)
tail(geno, n=4)
max(total)
#RowSums
total <- rowSums(geno[,4:6])
max(total)
#Disease-risk read
risk <- read.csv("C:Users/VivaA/2214/IntroBiolComp-2026/R/Datafiles/SNP_risks.csv", h=T)
str(risk)
#Add column
Not sure, program isn't working

#Read Smith
mass <- read.table("C:/Users/VivaA/2214/IntroBiolComp-2026/R/DataFiles/Smith2003_data.txt", h=T, sep = "\t")
str(mass)
head(mass)
#Get the number of rows
nrow(mass)
#Replace missing values
mass[mass[, 7] == -999, 7] <- NA
mass[mass[, 8} == -999, 8] <- NA
#Table
write.table(mass_table, file = "C:/Users/VivaA/2214/IntroBiolComp-2026/R/DataFiles/Smith2003_data.txt", sep = "\t", row.names=F, col.names=T)