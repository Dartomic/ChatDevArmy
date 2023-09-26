If I can finish the software that I am currently working on soon enough, which is not on GitHub yet, 
then this is something I am going to heavily modify.

The plan is to improve ChatDev's ability to manufacture software. The reason why I put "Army" at the
end of the title of this version of ChatDev, is because there is going to be an army of bots that spawn
in groupts of two for each module that needs to be developed. This design plan removes the ability of 
using the cartoon web interface, which I do like, but it doesn't fit the design plan. Instead of a 
development team that works on much more of the program per chatbot, this program is going to spawn
multiple sessions that are managed, and restarted if one of the sessions crash. I believe the design
I have in mind will allow for more software to be produced from managing the chat sessions in the way I
describe below. But perhaps the real ChatDev team will beat me to doing this. I hope so, because I don't
actually feel like writing this software. But I believe the design I have in mind for ChatDev is the 
Pandora's Box to getting Artificial Intelligence to writing complete software systems. 

So ChatDev did not produce a single program for me that worked, or worked correctly. When I adjusted the 
settings to match what I saw from other programs that were output, it actually was creating more functional
code in-line with what I requested, but then it would crash each time before finishing. I think it just needs
smaller chunks of information to work with, and it just needs more sessions to produce each smaller piece.




# Basic Plan
I think what I will do is make a bot that manages smaller, and nested, ChatDev sessions. The main bot 
will be within the same session as a designer ChatBot's session. The Designer Chatbot will be shut down
once it creates a very high level design, and then the army of nested bot sessions will spawn to work
on the smallest possible components of the software, each of them will close, and all of their work
will get combined into one project, instead of all of the individual temporary session projects that
they each work on. The sessions will be able to be restarted if they crash, which I believe will lead
to more projects being produced by ChatDev that get output which will are complete, and will work.








# Plan
This would potentially have the benefit of allowing a designer chatbot describe a higher level design of the program to identify inputs and outputs, and then identify all the tasks to be performed for its' processing, as well as a good label for each of the described tasks that need to be processed.

Then for the higher level processing designer: Two other chat bot sessions can take turns to identify all of the inputs and outputs for each of the processing labels of the tasks that were identified, while taking the inputs and outputs of the higher level design into consideration, and identify how different data components would best be represented, such as structs, linked lists, global variables, variables that would only be local to particular functions, etc. The reason they would take turns, and why there would be two of them, is so that they can check the work within the context that they are checking someone else's work, so that it will be more inclined to avoiding a bias that it was already correct, in order to output a more logical design. Also the reason why there would be two of them, is so that it would have two streams of prompts that could serve as the memory for each, and they may identify things in previous versions of the design that were actually useful.

Now for the lower level programming. I suppose there could be what is considered the "Dungeon Master" of the whole conversation. This could isolate each labeled task into separate and isolated conversations of three bots, one manager and two psuedocoders each. Each session, and sub-session, will have it's task noted in a file, perhaps an XML file. This could be in a nested format. Directories and files associated with each level will be logged into this file. The "Dungeon Master" writes to this main file if any of the sub-level XML files indicate an update to their nested structure. Each sub-level contains an XML file laying out the complete nested hierarchy of nested structures from from itself as a root, as well as the status of the particular session within the nest of layers. Status can be "processing" or "closed." All data within a session remain on the hosts computer.

The psuedocoders lay out the logic of each of the tasks, while identifying further sub-tasks. When identifying further sub tasks, they should use comments to briefly describe the job each need to perform, along with the inputs and outputs for the given sub-task. They would use psuedocode in order to allow for smaller prompts for the two cha tbots to work together on in order to reduce the chance of a conversation crashing, and to increase the chance of the design of the task being more logically correct.

Each manager within each of the groups has the same job as the "Dungeon Master." It can generate more sub-groups to work in isolation on the identified sub-tasks, in the same way it's group that it was spawned from did. Conceptually this would be like nested function calls, except in this scenario it would be nested job creation, unless there is a term for that already.

Once all the psuedocode is created for any given task, even for the higher levels of the nested jobs, the pseudocoder bots are swapped out with the programmers of the chosen language, and the work on translating the psuedocode into the language, on their own isolated source code files, until all of the sub-tasks are complete. So these can have a psudocode source code file saved, along with a real programming language source file saved. These could be saved for later improvement, correction, or for reference in the event of a crash of a chatbot that will need to be restarted for it to be prompted on what it needs to work on.

For each top-level task, there is a master source file. The manager also adds the file of the completed code of it's sub-tasks to a list. Once all sub-task of every every higher-level task, all the way to the root task, is complete; next-to lowest-level manager for the nests of each task copies the completed source code into it's master source-file, then closes out the sub-task conversation, thus ending the sub-session along with closing out its' bots within that session. This process takes place all the way to the very top-level, so that all of the conversations eventually come to a close, except for one.

Even though sessions become closed, the data from their session can be copied into a new session on the same level, in case an update needs to be made, or a correction needs to be made. This would allow for minimal quantity of token transactions within a session for an update of a component that needs to be made.

The inputs, outputs, and other data components that were previously identified would also be handled by a manager and two chat bots, in isolation at first, in order to design their implementation as derived from the higher-level design, but should become available for communication with the other chat bot conversations to only if any of them decide that something about that data needs to be changed, such as an int needing to really be a float. Another reason this section wold be handled a lot like the others in this way, is in the case that certain methods need to be developed in order to handle certain aspects of this data, such as methods needed in order to free memory from linked lists, change pages of linked lists, or other things that are only for accessing the data that the other tasks need to be able to do. The manager would relay this information to all other high-level managers of conversations that use that piece of information that needs to be updated, so that these managers can pass the message down to each of the sub-level managers that use the particular piece of data, so that each can make the necessary changes, or be given access to the specific methods related to the specific data that the particular tasks need to access. Due to it's job at making methods to access or modify the data, when it needs to do that, then this task group should be ran before the other top-level task groups.

This would allow for full modularity for each of the components of the software being designed. Each manager can restart a sub-session if it crashes, which would reduce the number of token transactions, in comparison to the token transactions required for the entire conversation of the whole program that is being developed, for what is needed to get that conversation back up-to-date in order for that particular dev team to get back to work from where it left off at on the particular module that it is currently working on. If the particular module that a group of two chat coders are working on crashes more than maybe twice, then perhaps the manager over them could prompt the team to redesign the piece to be composed of more than one function that will have their inputs and outputs in the comments above each of these sub-methods, which the manager will then spawn sessions for.

Each manager does not necessarily need to be a GPT chat bots themselves, since they have limited functionality. They do no designing. They simply pipe messages through chains of other managers, as well as close and open sub-sessions. So these do not need to cost in token transactions more than what they do when prompting a GPT model with a pre-defined prompt.


# Update
I thought of more stuff. All parts of the source code should have a reference ID that can be identified from within the XML file that contains the work and conversation history of that particular module.

Code Testing Process:

If the code is one that needs to be compiled:

The "Dungeon Master," or root session's non-LLM chat-bot can attempt to compile a copy of the code within an environment that will not mess up the host machine's files, once all the spawned sessions have completed their jobs. This would rely on instructions provided from prompting the designer chatbot on the command required to compile the code. (I have had GCC delete source code files due to some logical error I made in the C code itself.) Upon compilation failure, the ID number will be copied from the comment of the first section that the compiler identifies a problem with , the ID of the section before the identified failure point and/or the ID of the section(s) that call the section that the compiler identified the first problem with. All of this process can occur on a copy of the entire project. This process can repeat until the code compiles without error.

If the code is compiled, of if the code is a language that does not need to be compiled, is not doing the job it needs to do:

The program can notify the user that the program can now be tested, preferably in a VM. ChatDev can ask the user if the program works as expected. If yes, then the ChatDev program can just be closed. If no, then the user can tell it what did not work as expected, and ChatDev can respawn the designer session, ask it for the label of each task that may have errors that caused the stated problem, then spawn all of the associated high-level sessions, and ask these sessions which part of the pseudocode played a part in the stated problem, and repeat this as the sessions work all the way down to the sessions that
need to redesign to address the stated problem.

Once finished, then the code testing process repeats until the user is satisfied with the software that ChatDev produced.
