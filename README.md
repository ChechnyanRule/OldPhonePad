- I managed to implement a circular logic so that you can loop throught the letters, and come back at the beggining. if you press too many times, it loops back (press 7 four times outputs p, five times also outputs back p, etc.)  
- Handling of the circular logic: We assume that the user is typing as if he is using an old school phone keypad.
 Each key has multiple letters assigned to it, so what wwe need to do, is to figure out the correct letter based on how many times they pressed a given key. 
 So if you press "2" once, it will output "a". So far, so good. But what happens if he press "2" four times? Then is becomes "a" again (because "abc" loops).
 We have to use a formula based on the modulo to "cycle" the letters. 
 Once we get the remain of the euclidian division, we just "chop off" the group of consecutive letters down to the number of letters of the corresponding group. 
 And then, we select the letter in that group that corresponds to the remains of the euclidian division. For example, p belongs to the group "pqrs". It contains 4 letters. 
 So if the user inputs "7" 9 times consecutively, we do 9 % 4 = 1. So we get the letter "p" at the first index (which is 0).
