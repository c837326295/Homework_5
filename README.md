# Homework_5
The data presented in this repository includes cleaning up homicide data from
2007 to 2018 across the US. 

Load the csv file, data/homicide-data.csv, from the Washington Post
file_path <- "data/homicide-data.csv"
homicide_data <- read_csv(file_path)

This dataset provides a lot of awesome information including cities,
victim information, location, and the status of the case.

It's important to note that the date_reported column is **NOT** in date format.
Below I have included a snippet of code that I used to change the date.
I was focused on the city of Baltimore for this specific example.
baltimore <- homicides %>% 
   filter(city_name == "Baltimore, MD")
baltimore <- baltimore %>% 
  mutate("reported_date" = ymd(reported_date)) %>% 
  rename("date" = reported_date)
  
Enjoy!!