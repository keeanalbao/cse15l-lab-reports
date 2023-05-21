# Lab Report 4

## Step 1: Log into ieng6
For this step, I typed `ssh cs15lsp23ln@ieng6.ucsd.edu`, `<enter>`, my password, and `<enter>` again to log into ieng6.

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/b3256b80-fae4-4031-963e-8a04b8a96619)


## Step 2: Clone your fork of the repository from your GitHub account
For this step, I copied the HTTPS URL of the lab7 fork from my GitHub account, typed `git clone https://github.com/keeanalbao/lab7.git`
(using `<ctrl-v>` for the URL), and then `<enter>` into the command line. This cloned the repository 
into my ssh account.

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/053e51ef-6013-4988-88cd-bd77ec4e4a8f)

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/8dab1ac0-2562-4d35-9a0c-13bc4fab9551)


## Step 3: Run the tests, demonstrating that they fail
For this step, I changed to the lab7 directory by typing `cd l`, pressing `<tab>` to autocomplete it, and pressing `<enter>`. I then typed `ls` and `<enter>`
to list all the files/directories in lab7. Finally, I typed `bash t`, `<tab>` to autocomplete to `bash test.sh`, and pressed `<enter>`, which ran the tests.

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/f33afaaf-5885-491f-898d-f845b368fd6b)


## Step 4: Edit the code file to fix the failing test
For this step, I typed `vim L` and `<tab>` to autocomplete to `vim ListExamples`, then typed `.java` at the end, and finally pressed `<enter>`.

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/c0329795-bbf9-4f3c-ad6a-131bb1c20d86)

Next, the cursor was already on top of the `1` that I needed to change in ListExamples, so I simply typed `x` to delete the `1`.

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/b4aa4512-5580-4393-8151-5a04fa660eac)

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/4310cd43-08ef-49a0-812c-22e9c818457a)

I then pressed `i` to enter insert mode in Vim, and typed `2` to correct the error.

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/aefc96d2-7ca3-4e44-a4fc-8c1221508d02)

Finally, I pressed the `<esc>` key to switch back to normal mode in Vim, and then typed `:wq` to exit Vim and save the file.

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/cf391cf6-ce98-43e3-8d32-6b40f8869bf1)


## Step 5: Run the tests, demonstrating that they now succeed
For this step, I re-ran the tests by pressing `<up><up>` and then `<enter>` to run `bash test.sh` again.

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/043a5cdc-1047-40ac-bd99-3108de6051c8)


## Step 6: Commit and push the resulting change to your Github account
For this final step, I typed `git add L` then pressed `<tab>` to autocomplete to `git add ListExamples`, then typed `.java` at the end and pressed `<enter>`.
I then typed `git commit -m "changes"` and pressed `<enter>`. Finally, I typed `git push` and `<enter>`, my username `keeanalbao` and `<enter>`, and my GitHub password
and `<enter>`.

![](https://github.com/keeanalbao/cse15l-lab-reports/assets/88350907/217c8afe-8945-486d-a099-556e02d8052a)

