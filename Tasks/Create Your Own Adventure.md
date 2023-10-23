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
4. Create Folder for Quiz representation
	1. Populate with question--content-Fragments
		1. Build quiz, referencing questions and results appropriately
	2. Ensure folder is "orderable" and be sure that the first question is ordered as such. That is how I will be setting the first displayed question vs the hidden questions
5. Add quiz to component, and work out the UI
	1. Question as basically a header
	2. Help-text icon-button next to header (cobalt / dark-cobalt)
		1. on-click -> open help-text modal
			1. blue-transparent background
			2. X-out button top right (cobalt / dark-cobalt)
			3. click-out to close
			4. okay / cose button @ bottom
			5. Populate modal with `question.helpText`
	3. Question buttons displayed full-width
		1. radio-button behavior (radio-circle fills in)
		2. hover-state that follows brand-styles
		3. 
	4. 