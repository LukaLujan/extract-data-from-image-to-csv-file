# Extract data from a .jpg file and convert it into the proper .csv format file


First - sometimes parts of the jupyter code won't render properly on the github, in that case just copy paste github code link into this online aplication; 
https://nbviewer.org/

Anyway a first part is here;
https://nbviewer.org/github/LukaLujan/extract-data-from-image-to-csv-file/blob/main/part1-image%20processing.ipynb

And here is a second part;
https://nbviewer.org/github/LukaLujan/extract-data-from-image-to-csv-file/blob/main/part2%20-tessarect_regex_and_pandas_csv.ipynb


A main task of this project was to extract specific data from the pharmacy invoices(scanned documents in jpg or similar file format) and convert them to csv.file so they can be used in further analysis. 
Invoices are  stored in a folder "zadaci". And there is an example "goal.jpg" how it should look like in the end. 
I separated a task into two different jupyter notebook files.
In first notebook(part1) I was programing "universal" image processing tool. As you can see from folder "zadaci", all photos are somehow different. But I noticed the pattern , where all interesting data is on on specific location of each invoice(between some specific horizontal lines). Using Python CV2 library tools, and some coding I managed to make a program that can handle any type of those 5 different invoices and crop the part of the photo that has all information we need. There were some challenges of course that I manage to overcome, but you can read about those challenges in the comments of the first notebook(part1) along with the code.
In second notebook(part2), I used "tesseract library" to extract data. Then I used regex to further extract data on the way I needed. It was converted to data frame and saved to csv file. Mission completed - almost. Problem was that in the next photo , data that was extracted was in totally different format, and in this case regex will not work "universally" and I need to re-type regex code for each photo. I talked with some more experienced people, and they agreed that this problem can not be solved with "universal" regex, some more complex model may be used in this case, but that is something that I will do next time.
