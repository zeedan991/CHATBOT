Java ChatUser Thread Example
This project demonstrates a simple multithreaded chat simulation in Java, showcasing thread priorities, lifecycle control, and basic synchronization concepts.

Overview
The program creates two chat users represented as threads — Bob and Alice. Each user sends a series of chat messages with controlled timing. The threads run concurrently with different priorities, and the program demonstrates key thread control operations such as pausing, resuming, and stopping threads.

Key Features
Thread Priorities: Bob runs with maximum priority while Alice runs with minimum priority.

Message Simulation: Each user sends 5 messages, with a 500ms delay between messages.

Thread Control: The main program can pause, resume, and stop the user threads dynamically.

Lifecycle Management: Uses thread state checks and join() to coordinate thread completion.

Volatile Flags: Uses volatile booleans to manage thread pause and stop states safely.

How It Works
Two ChatUser threads are created and started.

Bob's thread is given high priority, and Alice's low priority, to demonstrate priority effects.

The main thread pauses Bob, waits for Alice to finish chatting, then resumes Bob.

Finally, the main thread stops Bob and waits for termination before ending the program.

Code Breakdown
Main Class:

Creates and starts threads.

Controls thread states with pause, resume, and stop.

Uses isAlive() and join() for thread monitoring and synchronization.

ChatUser Class (extends Thread):

Sends messages in a loop while running is true and not paused.

Sleeps 500ms between messages.

Methods to pause (Pausechat()), resume (Resumechat()), and stop (Stopchat()) the thread.
