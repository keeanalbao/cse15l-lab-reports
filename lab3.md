# Lab Report 3

# Researching the `find` Command

##  `-type` Command-Line Option

The `-type` command allows the user to search for files by type. 

This is useful because it allows the user to perform actions within their desired directory on just the types they specify. 

In this first image, I searched for all the file types (`-type f`) in the directory I gave.

![Screenshot 2023-05-04 153354](https://user-images.githubusercontent.com/88350907/236343919-5749850e-1456-4bfc-885c-5fe00e9677cf.jpg)

In this second image, I searched for all the directory types (`-type d`) in the directory I gave.

![Screenshot 2023-05-04 153423](https://user-images.githubusercontent.com/88350907/236343931-fde871a1-fdad-44ed-8711-e38ae0860661.jpg)

(Source: ChatGPT. I asked "can you tell me some command-line options using the command -find in bash")


## `-maxdepth` Command-Line Option

The `-maxdepth` command allows the user to limit the depth of the search.

This is useful because it allows the user to only search for files within a few specified directories, and not in subdirectories that are deeper than a certain level.

In this first image, I only searched for the directories that had a max depth of 2 relative to `stringsearch`.

<img width="348" alt="Screenshot 2023-05-05 011215" src="https://user-images.githubusercontent.com/88350907/236408386-e0f9329d-bbc0-453a-b436-2006e21ffa23.png">

In this second image, I only searched for the *text* files that had a max depth of 3 relative to `stringsearch`.

<img width="431" alt="Screenshot 2023-05-05 011241" src="https://user-images.githubusercontent.com/88350907/236408424-cf5dd454-9e1a-4f3d-a31a-515160a68241.png">

(Source: ChatGPT. I asked "can you tell me some command-line options using the command -find in bash") 


## `-size` Command-Line Option

The `-size` command allows the user to search for files by size.

This is useful because it allows the user to search for small, medium, or large files and determine if they want to keep them or not.

In this first image, I searched for all files with a size of exactly 2 bytes. 

![Screenshot 2023-05-04 225157](https://user-images.githubusercontent.com/88350907/236385880-ee0d8dde-9d24-4a06-af5d-c04a725f850c.jpg)

In this second image, I searched for all files with a size of less than 3 kilobytes.

![Screenshot 2023-05-04 225218](https://user-images.githubusercontent.com/88350907/236385925-7f31786a-9c49-45d4-889b-8e9c119fa3d1.jpg)

(Source: ChatGPT. I asked "can you tell me some command-line options using the command -find in bash") 


## `-delete` Command-Line Option

The `-delete` command allows the user to delete all files or directories that match the search criteria.

This is useful because it allows the user to free up disk space by removing files that they don't need or that are too large. It also allows them to delete a  group of files quickly by giving a specific criteria.

In this first image, I searched for all the text files within the `biomed` directory and deleted them.

<img width="419" alt="Screenshot 2023-05-05 003427" src="https://user-images.githubusercontent.com/88350907/236401994-a6087b0e-91dd-4992-a5bd-b1fdfd26a117.png">

In this second image, I searched for all the files that started with `pmed` within the `plos` directory and deleted them.

*Before:*

<img width="830" alt="Screenshot 2023-05-06 115245" src="https://user-images.githubusercontent.com/88350907/236641732-1669eb57-eb3b-43bd-a086-7ba6fc58be74.png">

*After:*

<img width="866" alt="Screenshot 2023-05-05 003921" src="https://user-images.githubusercontent.com/88350907/236402053-fec07291-be04-4da0-961d-af57462a5c91.png">

(Source: ChatGPT. I asked "can you tell me some command-line options using the command -find in bash") 
