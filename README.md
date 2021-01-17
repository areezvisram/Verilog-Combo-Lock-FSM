# Verilog Combo Lock FSM
A Moore finite state machine designed in Verilog that creates the functionality of a combination lock.

The Verilog file containing the design is __combolock.v__

### Functionality:
- 4-input code is set as the desired unlock combination
- On Altera Board, user enters 4-input code, then "presses" Enter (push Enter input switch HIGH)
- If input matches stored unlock combination, door opens (Open output goes HIGH)
- Door stays open until Enter is "pressed" again, which closes the door
- If two incorrect combinations entered, alarm output goes HIGH
- Alarm can be cancelled by enabling reset, achieved by push Reset input HIGH
- To enter new unlock combination, set to old unlock combination and "press" Change (push Change input switch HIGH)
- If done correctly, output New goes HIGH
- Set new combination, then push Enter or Change HIGH to confirm the new combination
- Hex display used to show output
- Possible output combinations:
  - All outputs LOW -> '-'
  - Alarm HIGH -> 'A'
  - New HIGH -> 'n'
  - Open HIGH -> 'O'
 
### Finite State Machine Design:
- The state diagram for this FSM:

- The block diagram for this FSM:
![Block Diagram]https://github.com/areezvisram/Verilog-Combo-Lock-FSM/blob/master/images/Block%20Diagram.jpg
