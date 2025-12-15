# Identify: 
We have multiple buttons that control the intake in different ways. But there is a problem; the code has no functionality coded for multiple buttons being pressed. Currently, when multiple buttons are pressed, it always prioritizes whichever button we put in the code first. ​This leads to intuitive behavior when accidentally or purposely pressing 2 buttons.

# Brainstorm:
I could leave it, there are use-cases for having a “highest priority” intake button, but it gets a little buggy with the 3 different types of buttons we have defined. We could code it to ignore all other intake button inputs if one is still active. This would solve the problem by avoiding the problem, but I believe that it would be confusing and temperamental. Another solution would be to prioritize the newest intake button press. This would make it so any time an intake button is pressed, the corresponding function is done, regardless of other active intake buttons.​

# Select:
I chose prioritizing the newest button press. This is very intuitive and it solves the problem elegantly. If a new button is pressed, that function comes active even if the other button has not been released yet. ​

# Implement:
I started by expanding my button state header from earlier. I added another section, separate from the button type section, that handles priority stacks. I codded in a counter system that counts up every cycle of the main loop. Then, when a new button is pressed, (It checks by seeing if the button was not previously active and is now active), it records the time when the button was pressed by setting a variable equal to the current value of the counter. Then, every loop, it finds the button counter with the highest value and checks to see if the corresponding button is still in an active state. If it is not, it goes to the next highest highest counter and checks its button state, and so on. This satisfies our original problem by checking the button that was most recently pressed first. But it also solves another problem. With a highest counter system like this, the code always sets the button that was most recently pressed as the active state. This works intuitively 90% of the time, but if we were to be holding a button, and then while still holding that button, accidentally bump another button, the code would set the new button as the active state, as expected. However, after releasing the button, the code would just stop the action, regardless of the fact that the first button is still pressed. So, by checking the next highest button counter when the button with highest counter is inactive, we solve this problem. This makes it so if we press and release a button while another one is still held, the code would go back to the old button’s function. 

# Test: 
When testing, the system appears to work perfectly, but if we logically think about the code, we can identify a minor problem. The system relies on a counter that goes up infinitely until the code stops.​


# Repeat: 
## Identify: 
We have a counter that goes up infinitely, but variables in code cannot be infinite, they have a defined range. This means that if we waited long enough, the counter would add 1 to its maximum number, overflow, and drop back down to 0, causing unexpected behavior. ​

## Brainstorm: 
I could extend our time by making the counter have a bigger range. I could make the code detect when the counter gets to or close to its maximum number, then subtract a large amount from the main counter and the individual button counters. I could ​make the counter only change when a button is pressed, instead of relying on time. I could replace the counter with a different system entirely, perhaps a system that rearranges the button priorities. I could just leave it, the problem would only happen if we waited long enough, and even then, it would only make the functions behave incorrectly just the first time a button is held and another one is pressed at the same time.

## Select:
Leaving it be seems irresponsible; I believe that I should fix any bug I can find a solution for. Making the counter longer would likely make it never a problem in a competition or during testing, but it still feels wrong to just leave a bug in the code. Similarly, making the counter dependent on when a button is pressed would make it take almost 4.3 billion button presses before noticing a problem, but it still feels wrong to leave an issue in the code. Subtracting would work by making sure would never be able to reach the maximum value. The math would get complicated on edge cases, but it would be doable.  using a priority stack seems the most responsible. It gets rid of any possibility of overflow issues and does not require complicated math. 

## Implement:
To start, I completely removed the counter system. After removing the old system, I started on a priority stack, specifically a LIFO Last In, First Out stack. I then created a vector that stores the names of the intake states, namely "IN", "OUT_TOP", "OUT_MID", and a few more.  Then when a new button is pressed, or in other words, a button is pressed that was not previously pressed, it removes the corresponding name from the vector and adds it back in at the start. It then checks if the corresponding button for first name in the vector is still active, and if not moves on to the next name in the vector, and so on. 

## Test: 
Everything worked as expected, however, our driver did not like that the toggle buttons would persist after another button is pressed and released. To fix this, I adjusted the code so that any time a new button is pressed, all toggle buttons are set to not active. 


	Linus 11/12/2025