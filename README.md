# Portfolio
mes compétence 

#### url where the data is located
url <- "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/WmJTNZlA5hEqXzFUOxCu8w/lax-to-jfk-tar.gz"
### download the file
download.file(url, destfile = "lax_to_jfk.tar.gz")
## untar the file so we can get the csv only
untar("lax_to_jfk.tar.gz", tar = "internal")
# read_csv only 
sub_airline <- read_csv("lax_to_jfk/lax_to_jfk.csv",
                     col_types = cols(
                      'DivDistance' = col_number(),
                      'DivArrDelay' = col_number()
                      ))

