** Starting with R and TraMineR**

library (TraMineR)

** Look at the help page of biofam data.Find out which are the columns containing the sequence data.**

data (biofam)
?biofam
biofam [1:1, 1:27]
*Columns 10-25 contain the sequence data.*

** Look at the first six rows of the data frame**
head (biofam)
biofam [1:6, 10:25]

** Create the state sequence object.**
biofam.seq<-seqdef (biofam[, 10:25])

** plot the first ten sequences**
seqiplot (biofam.seq)

** Plot the ten most frequent sequences. **
seqfplot (biofam.seq)

** Plot all sequences sorted **
seqIplot (biofam.seq, sortv="from.end")

** Plot the sequence transversal distribution **
seqdplot (biofam.seq, border=NA)

** Display the first 10 sequences in extended form .**
biofam.seq[1:10,]

** Display the first 10 sequences in compact form**
print (biofam.seq[1:10,],format="SPS")
