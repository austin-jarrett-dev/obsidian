##### Ticket: [WE-817](https://firstfinancialbank.atlassian.net/browse/WE-817)
##### Title: 
Create Your Own Adventure -- New Component
##### Description: 
FFB is asking for a new component to house an interactive 'quiz' for the user. The quiz will include a series of questions, and the respective answers (limited to 2 answers). As the user selects an answer the Quiz will progress -- either prompting the next question to appear, or displaying a result

---

![[CYOA Diagram.svg]]

## Development Planning

### Expected Steps
1. Create Component
	1. Single field for "Quiz Path" / "Parent Path" that points to the asset folder in which we are storing the questions for the component
2. Create Content Fragment Model
	1. Question Text (Single Line Text)
	2. Help Text (Multi Line Text / Rich Text?)
	3. Answer 1
		1. Answer 1 Text (Single Line Text)
		2. Answer 1 Next Step (Content Reference)
		3. Answer 1 Next Type (Enumeration <<Question / Result>>)
	4. Answer 2
		1. Answer 2 Text (Single Line Text)
		2. Answer 2 Next Step (Content Reference)
		3. Answer 2 Next Type (Enumeration <<Question / Result>>)
3. Create Results Experience Fragment
	1. Make Variation for each result