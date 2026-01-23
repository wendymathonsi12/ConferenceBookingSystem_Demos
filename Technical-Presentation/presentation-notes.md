Introduction & Goals
- Welcome everyone. Today we’re looking at the engine room of our project: how we actually work together without breaking each other's code. We’re building a Conference Room Booking System, and because we have multiple people touching the same files, our Git workflow is our most important safety net.
        •	Timing: 2 minutes
	•	Key Insight: Focus on the " Commit"
Branching Strategy (Feature Branch Workflow)
- We never commit directly to the main branch. Think of main as the "sacred" version of the app that is currently live. Instead, we use a feature-branch workflow. If you’re working on the "Calendar View" or "User Authentication," you create a branch named feature/description. This keeps your experimental code isolated until it’s battle-tested.
	•	Timing: 2 minutes
	•	Key Insight: Explain that short-lived branches are better than long-lived ones to avoid "merge hell."
	•	Shutterstock
Explore



The Anatomy of a Good Commit
- Don’t just write "fixed stuff" or "updated CSS." A good commit should explain what changed and why. In our booking system, a commit like "Add validation for double-booked rooms" is much more helpful six months from now than "update logic." Smaller, frequent commits are easier to debug than one giant "finished the project" commit.
	•	Timing: 2 minutes
	•	Key Insight: Focus on the "Atomic Commit" principle—one change, one commit.
Pull Requests & Peer Review
- The Pull Request (PR) is where the magic happens. This is our "quality gate." Before code moves into main, at least one other person needs to look at it. We aren't looking for typos; we're looking for logic errors—like, "Does this code accidentally allow someone to book a room for -5 minutes?" or "Will this break the database connection?"
	•	Timing: 3 minutes
	•	Key Insight: PRs are for mentorship and knowledge sharing, not just policing.

Handling Merge Conflicts
- Conflicts happen, especially when two people edit the RoomList.js component at the same time. Don't panic. We handle this by pulling the latest main into our feature branch regularly. If a conflict occurs, Git will mark the file. We'll decide which version of the "Booking Button" logic wins, test it locally, and then proceed.
	•	Timing: 2 minutes
	•	Key Insight: Demonstrate that conflicts are a natural part of collaboration, not a sign of a mistake.

Summary & Next Steps
- To wrap up: Branch for every feature, commit with intent, and respect the PR process. This workflow ensures that our booking system remains stable and that we can onboard new developers quickly without them fearing they'll break the production environment.
