

Part 1: The Local Setup
System/Screen: Terminal (VS Code) and the GitHub Repository web interface.
	•	Action: Open the terminal in the room-booking-system project.
	•	Command: ```bash git checkout main git pull origin main git checkout -b feature/add-amenities-list
	•	Talking Points: * "I’m starting from a clean, up-to-date main branch."
	•	"I’m creating a descriptive branch name so the team knows exactly what I’m working on."
	•	Proof: Reinforces the rule of never working directly on main.

Part 2: Commits
- System/Screen: VS Code Editor.
	•	Action: Open RoomDetails.js. Add a new array called amenities (e.g., Projector, Whiteboard). Save and commit.
	•	Command:
Bash

git add RoomDetails.js
	•	git commit -m "feat: add basic amenities array to RoomDetails"
	•	



	•	Talking Points: * "Notice I’m not finishing the whole feature at once. I’m making a small, logical save point."
	•	"The commit message follows our team prefix feat:, making the logs searchable."
	•	Proof: Demonstrates clean history and accountability.

Part 3: The Pull Request (PR)
System/Screen: GitHub Web Interface.
	•	Action: Push the branch and open the "Compare & Pull Request" page.
	•	Command: git push origin feature/add-amenities-list
	•	Talking Points: * "I’m adding a description of what I changed and tagging a teammate for review."
	•	"I’ll point out the 'Files Changed' tab so the reviewer can see exactly what lines are new."
	•	Proof: Reinforces the PR as a quality gate.

Part 4: Handling the Conflict (The "Real World" Scenario)
System/Screen: Terminal and VS Code.
	•	Action: Simulate a teammate merging a change to the same file. In the demo, switch back to main, make a quick change to the same line in RoomDetails.js, commit, and push. Then, try to merge main into your feature branch.
	•	Command:
Bash

git checkout feature/add-amenities-list
	•	git merge main
	•	



	•	The Conflict: VS Code will highlight the "Current Change" vs. "Incoming Change."
	•	Action: Manually resolve the conflict by keeping both changes, then finalize the merge.
	•	Talking Points: * "Git flagged this because someone else edited the room logic while I was working."
	•	"I’m resolving this locally before it ever hits the production code."
	•	Proof: Proves that the system prevents accidental overwrites.

Part 5: Final Verification
System/Screen: Local Browser (localhost:3000).
	•	Action: Refresh the Conference Room Booking app.
	•	Talking Points: * "The code is merged, the conflict is gone, and as you can see, the 'Amenities' list is rendering correctly."
	•	"Now I can safely hit 'Merge' on GitHub."
	•	Proof: Confirms that workflow discipline leads to a working product.
