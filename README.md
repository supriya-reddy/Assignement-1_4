# Assignement-1_4
1. Read multiple JSON files into a directory to convert into a dataset.
    I have files text1, text2, text3 in the directory JSON.
    Ans:  
                       
          install.packages(“rjson”)
          Library(“rjson”)
          # read the json file as follows: 
          result <- fromJSON (file = “file.json”)
          We can convert the extracted data above to a R data frame for further analysis using the as.data.frame() function.
           
           json_data.frame <- as.data.frame(result)


2. Parse the following JSON into a data frame.

          js<-'{
          "name": null, "release_date_local": null, "title": "3 (2011)",
          "opening_weekend_take": 1234, "year": 2011,
          "release_date_wide": "2011-09-16", "gross": 59954
           }'
3. Write a script for Variable Binning using R.
Ans: When we need to convert the continuous data into the categorical data, the process is called the Variable Binning.
Eg:

            Age is a continuous variable,
            10,15,20,25,20,23,25
            We can categorise like,
            10-15 -> T
            15-20 -> Y
            20-25 -> Z
            Ifelse( x>=10 & x<15, “T”, ifelse ( x>=15 & x<20, “Y”), ifelse( x>=20 & x<25, “Z”)))

