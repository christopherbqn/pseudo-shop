# Final Project Retrospective

## Team Members
- Student 1: Christopher Gilbert Bayquen
- Student 2: Jerome Yang

## 1. How did you divide the work between you and your partner?
_(Who worked on which features? How was the work assigned or negotiated?)_

* **Student 1 or Christopher** focused on **Feature 3: Product Management** and **Feature 4: Display Storefront**. These were grouped because displaying products naturally follows from managing them.
* **Student 2 or Jerome** focused on **Feature 2: User Registration and Login** and **Feature 1: Filter Products by Attributes**. User management was independent, allowing early parallel work. Product filtering was assigned to Student 2 as it logically followed the product data structure and display established by Student 1. The main.pseudo file was contributed by both the students to implement each of their respective features, having student 1 finalize the main application flow.


## 2. What Git strategies or commands helped you most during the project?
_(E.g., branching, rebasing, frequent commits, etc.)_

* `git checkout -b <branch-name>`: Essential for creating feature branches, ensuring work isolation.
* `git add <file(s)>`: Staging changes for commit.
* `git commit -m "Type(scope): Message"`: Making descriptive, atomic commits. The conventional commit style was very helpful for clarity.
* `git push origin <branch-name>`: Pushing local changes to the remote repository.
* `git pull origin main`: Crucial for keeping feature branches up-to-date with the `main` branch before merging, and for fetching the latest changes to `main` itself.
* `git merge <branch-name>`: Integrating completed feature branches into `main`.
* **Pull Requests (simulated):** While not direct commands, the PR workflow encouraged code review and discussion before merging, leading to higher quality code and fewer issues.
* `git status`: Frequently used to check the state of the working directory and staging area.


## 3. Describe a merge conflict you encountered. What caused it and how did you resolve it?
_(Include any lessons learned or techniques used to resolve the issue.)_

Merge Conflict Encountered: 
The merge conflict occurred in the `Main.pseudo` file. Christopher was working on the `feat/product-management` branch and he added the `handle_add_product()` function. Simultaneously, 
Jerome is working on the `feat/user-auth`, added the `login_page()` on the main.pseudo in a different section of the same file. When student 1 created a pull request on the main branch and after completing the commented changes from the review and got approved to the main, then student 2 created a pull request of `feat/user-auth` into `main`, Git detected overlapping changes in `main.pseudo`, resulting in a merge conflict, thus student 1 in the pull request forum requested a change as its review on the pull request.

Merge Conflict Resolution:
Student 2 resolved the conflict as it occurred on its PR on github, not showing it can automatically merge. To fix the issue, Student 2 first pulled the latest changes from `main` into their `feat/user-auth` branch. This pulled Student 1's changes from the `feat/storefront-display` merge, causing the local conflict. Student 2 then manually edited `Main.pseudo`. They identified the sections marked by Git's conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`). They carefully combined both sets of changes, ensuring that all necessary sections were correctly integrated and ordered logically.
After resolving the file, Student 2 staged the changes and created a merge commit. Finally, student 2 pushed the resolved feature branch and then the PR on github then showed that it can now merge, after student 1 reviewing the requested changes, student 2 merged it into `main`.



## 4. What were the biggest challenges you faced as a team?
_(This can include communication, Git usage, or coordination.)_

* **Coordinating parallel development:** Ensuring we weren't stepping on each other's toes too much, especially with the shared `Main.pseudo` file. One of the challenges we also faced was the implementation of the Pull Request in Github as we were not that familiar with the process of it yet– we experimented with closing and re-opening the pull requests when we encountered merge conflicts to see if it was necessary to open new pull requests when changes were needed to be done again before merging. Overall, the main challenge was maintaining clear and proper communication to ensure continuous parallel development, including defining file ownership and clarifying our collective approach to solving the problem.

## 5. What did you learn about using Git in a collaborative setting?
_(Any insights or habits you’d apply in future projects?)_
 
* **Importance of feature branching:** It's indispensable for isolating work and preventing direct conflicts on the `main` branch until features are ready and reviewed.

* **Regular pulling from `main`:** Frequently pulling changes from the `main` branch into feature branches helps identify and resolve conflicts earlier and in smaller, more manageable chunks.

* **Clear commit messages:** Descriptive commit messages (using a convention like Conventional Commits) are vital for understanding the history and intent of changes, especially in a team environment.

* **Collaborative conflict resolution:** Conflicts are inevitable. Understanding how to manually resolve them and communicating during the process is a key team skill. The use of github pull request feature provided a key platform in resolving resolution collaboratively by lending developers a place to communicate review comments, adding a forum and a history on how an issue has been resolved, especially important in tracking developmental issues and how it was solved.

* **The value of Github Pull Requests:** They serve as a critical checkpoint for code quality, consistency, and team alignment before code hits the main codebase.


## 6. How would you improve your workflow next time?
_(Think about technical habits and teamwork practices.)_


* **Pre-emptive conflict avoidance:** For shared files like `Main.pseudo`, define clear areas of responsibility or create specific "integration points" that only one person modifies at a time, or where modifications are highly coordinated.
* **Automated testing:** While not directly part of pseudo-code, in real projects, integrating automated tests in the CI/CD pipeline like github workflow would help catch issues earlier, including those arising from merges.


## 7. Optional: Any feedback on the activity?
_(What worked well? What was confusing or could be improved?)_

The purpose of the `Main.pseudo` file was unclear. Although we understood the prompts for each feature, we were confused about how they fit together and what the final goal was. This made us wonder whether to simplify our approach or build a user interface. We chose a pseudo-interface to better connect the functions. 


