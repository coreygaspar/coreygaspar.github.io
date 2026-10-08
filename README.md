# CS-499 ePortfolio

## Introduction
Hello, my name is Corey Gaspar and welcome to my ePortfolio! As of writing this, I am finishing up my Bachelor of Science degree in Computer Science. This ePortfolio serves as a way to showcase the knowledge and skills I've obtained throughout the computer science program and highlight my growth in software development, algorithms and data structures, databases, and security.

<br>

## Self Assessment
Throughout my time in the Computer Science program at Southern New Hampshire University, I have developed a wide range of technical and professional skills. My coursework has given me experience in a variety of areas, from writing basic code to creating secure, full stack applications. It has also helped me become more comfortable learning new technologies and working through problems when I don't immediately know what the solution is. As I've progressed through the course, I've learned that computer science is more than just writing code. It requires careful planning, communication, testing, problem solving, and understanding the needs of the end user.

The most important skill I've developed from this program would be problem solving. Sometimes, looking at requirements all at once can be overwhelming. I've learned that breaking down problems into smaller parts and considering different ways to solve them can make them more manageable. I've also learned that a solution to a problem should not only work, but should also be efficient and appropriate for the given situation. This has helped me become more comfortable with working through difficult problems instead of becoming overwhelmed by them.

Another important area I've developed is my ability to work with existing software. Throughout the program, there have been projects where I had to understand the code that was already written before I could make any changes to it. This taught me to take my time and understand how different parts of an application work together before making changes. I've also gained experience in testing any changes I make and fixing problems if something goes wrong.

Communication and collaboration have also been important parts of my development. Most, if not all of my coursework has required me to explain technical information through written assignments, journals, discussion posts, and project work. I've learned how to gauge my audience to understand how technical information should be explained. For example, I would simplify my explanation for end users with limited technical knowledge, while I would feel comfortable being more detailed with developers or engineers. I've also learned the importance of considering feedback and different perspectives when working on a project. Everyone has different ideas of what the end project should look and feel like, so incorporating those perspectives can help create a better final product. Being able to communicate clearly while also being open to other ideas is something I know will being important moving forward.

Finally, security has become another skill that I have developed from this program. I've learned that security should be considered throughout the entire development process rather than treated as an afterthought or something that should be incorporated later on. I've gained experience with areas like user authentication, data validation, and protecting sensitive information. I've learned the importance of protecting PII and the consequences that can come from neglecting to do so. I've also learned that small changes in a program can cause larger problems later on if not tested properly. This has helped me develop a stronger security mindset that I can use in my future work.

<br>

## Code Review
[Click here to view my code review](https://drive.google.com/file/d/15FX3ki2ujTkb_hB412PzoKDNIRw0Utbg/view?usp=sharing)

<br>

# Enhancement One: Software Design and Engineering

## Description
The artifact I selected is my Travlr Getaways web application, which I originally built throughout the CS-465 course. The application allows users to view travel information, while authenticated users can add and edit trips. The application uses Angular for the front end, Express and Node.js for the backend, and MongoDB with Mongoose for data storage.

For my CS-499 enhancement, I added the ability to delete trips. This completed the main CRUD functionality for the trip data by allowing authorized users to create, read, update, and delete trips.

## Justification
I included the Travlr Getaways application because it demonstrates several software development skills that I have gained during my time in the Computer Science program. The artifact includes a frontend application, backend API, database, authentication methods, and communication between all of the different parts of the application.

The original application already allowed users to add, view, and edit trips. The enhancement added the missing delete operation. I added a delete method to the Angular trip data service, a delete endpoint to the Express API, and a Delete Trip button to the trip cards. The button is only able to appear if the user is signed in. I also added a confirmation prompt so that a user has to confirm before a trip is removed, which reduces the possibility of a trip accidentally being removed.

This enhancement improved the application by making the trip management functionality more complete. It also gave me experience working across the frontend and backend instead of treating the enhancement as its own isolated change. I had to make sure the frontend request, API route, controller, and database all worked together as expected.

## Course Outcomes
I met the course outcomes that I planned to address with this enhancement in Module One. The main outcome supported by this enhancement is demonstrating the ability to use well-founded techniques, skills, and tools to implement computer solutions that provide value and accomplish software development goals.

The enhancement also supports the security mindset outcome. The delete operation is protected by the existing JWT authentication token, meaning an unauthenticated user can’t manage trips. This made it clearer as to why security should also be considered, rather than just focusing on if the feature works.

My outcome-coverage plan still hasn’t changed. I still plan to use the Travlr Getaways artifact to demonstrate software engineering and design skills while also addressing security and database concepts through other enhancements planned for the project. I still have another use for this project later on.

## Reflection
This enhancement taught me more about how the different parts of a web application work together. I had to make sure the button on the website connected to the back end and that the back end could remove the trip from the database. I also learned that I didn’t have to add a new delete component. My TripDataService already had the functionality planned for deleting a trip. All I needed to do was build out that functionality and connect the different parts of the application.

One of the main challenges was making the enhancement without breaking the functionality that was already working. I had to work with the existing structure of the application and make specific changes rather than rewriting existing code. I ran into an issue where my application ran into a 404 error when trying to sign in. I accidentally removed the “login” and “register” functions which is why I ran into that issue. Testing after each change helped me confirm that authentication and existing functionality continued to work.

I also learned more about the importance of testing an enhancement from the user’s perspective. The delete button needed to call the correct API endpoint, the API needed to find the correct trip, and the database needed to remove the trip. Adding a confirmation prompt was also useful for preventing accidental deletion.

## Repository
[Enhancement One Repository](https://github.com/coreygaspar/Enhancement-One-CS499)

<br>

# Enhancement Two: Algorithms and Data Structure

## Description
The artifact I selected for this milestone is the Pirate Intelligent Agent from CS-370. It is a Python program that uses a deep Q-learning algorithm to train a pirate agent to navigate an 8x8 maze and reach the treasure at the bottom of the grid. The original project uses Python, TensorFlow, and Keras within a Jupyter Notebook environment, as well as experience replay to train the agent.

For my CS-499 enhancement, I improved the Q-training process by adding a target network and an early-stopping check. I also fixed the testing process so the agent only chooses valid actions when the completion check is running.

## Reasoning
I selected this artifact because it demonstrates my ability to work with algorithms and apply changes to an existing program. The artifact uses deep Q-learning, experience replay, and Q-values to help the agent learn how to move through the maze.

My original plan was to improve the efficiency of the training process by lowering the exploration rate over time and adding early stopping. As I worked on the enhancement, I changed part of the plan and added a target network instead. The target network is updated every 50 epochs using the weights from the main model. This gave the training process a more stable target while the agent learned.

I also added an early-stopping check. The program checks the agent’s win rate during training and runs a completion check when the win rate reaches 100%. If the agent can complete the maze consistently over and over, then training stops successfully.

## Course Outcomes
I was able to meet the course outcome below:

**Design and evaluate computing solutions that solve a given problem using algorithmic principles and computer science practices and standards appropriate to its solution while managing the trade-offs involved in design choices.**

This enhancement supports the outcome because I improved and tested the Q-training algorithm to solve the pirate’s pathfinding problem. I had to understand how the model, target network, experience replay, and the agent’s actions worked together.

I also had to make changes based on the results of my testing. The completion check problem showed me that improving one part of the program can introduce new issues to other parts of the system. After fixing the valid-action logic, the program was able to correctly test the trained agent and stop training when the completion check passed. My outcome-coverage plan has not changed after this enhancement. This artifact is a good representation of my skills in algorithms, problem solving, testing, and evaluating a computing solution.
  
## Reflection
When enhancing this artifact, I learned more about how Q-learning works and how the different parts of the training process work together. Adding the target network helped me understand how using a separate network can make the training process more stable. I also learned that testing the algorithm is crucial to its success.
  
One of the biggest challenges was getting the process running in my current environment. Previously, I had this running in a virtual machine with the packages and software preconfigured. I had to install the correct version of Python and several other packages before I could test my changes.

Another challenge happened when the agent reached a 100% win rate but continued training. I had to look through the completion check to find the problem. I found that the testing function was choosing the highest Q-value without checking if the action the agent took was valid. I changed it so that the agent only chooses valid actions during the test. After this change was made, the completion check worked, the training stopped early without having to run through all 1,000 episodes, and the agent found its way to the treasure.

## Repository

<br>

# Enhancement Three: Databases

## Repository


