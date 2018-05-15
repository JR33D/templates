# Code Review Guide

> A friendly guide for reviewing code--and not each other--.

## Why reviews?

Code reviews are incredibly important step to the development process. Our goals
when reviewing code are to:

- expose bugs before they make it to production;
- ensure a consistent quality in the codebase;
- create an environment for sharing knowledge and developing skills;
- encourage open communication between the entire team.


## Tips for a successful review

For a code review to be successful, we all need to be on the same page. To help
accomplish this, everyone should follow these tips.

### For everyone

- Remember that we're reviewing the code, not the author. Nothing should be
  given or taken taken personally.
- There is often more than one way to approach a solution. Discuss tradeoffs and
  reach a resolution quickly.
- Refer to the style guides whenever there's a discussion that can't be resolved.
- Ask questions rather than make statements. ("What do you think about...?")
- Ask for clarification if the code or comments are unclear. ("I didn't understand.
  Can you clarify?")
- Support opinions with reason and facts: "I recommend this approach instead because...."
- Avoid selective ownership of code. ("mine", "not mine", "yours")
- Avoid using terms that could be seen as referring to personal traits.
- Be explicit, people don't always understand your intentions online.
- Be humble. ("I'm not sure - let's look it up.")
- Don't use hyperbole. ("always", "never", "endlessly", "nothing")
- Don't use sarcasm.
- Keep it real. If emoji, animated gifs, or humor aren't you, don't force them.
  If they are, use them with aplomb.
- Talk offline if there is too much back and forth. Post a follow-up comment
  summarizing the discussion.
- If you've paired on the code or otherwise discussed it in detail outside of the pull request,
  note that in the PR so it's clear to everyone that the work has had appropriate collaboration.
- Praise team members when they create exemplary work or suggestions.

## For code reviewers

- Review the code, make comments, and/or merge within 1 week of being assigned a pull request.
- Understand why the code is necessary (bug, user experience, refactoring)
- Seek to understand the author's perspective.
- Clearly communicate which ideas you feel strongly about and those you don't.
- Identify ways to simplify the code while still solving the problem.
- Offer alternative implementations, but assume the author already considered
  them. ("What do you think about such-and-such here?")
- If discussions turn too philosophical or academic, move the discussion to a new
  issue or offline. In the meantime, the **author has the final say on the current
  implementation**.
- Avoid focusing on trivial issues. This is often termed [bike-shedding](https://en.wikipedia.org/wiki/Law_of_triviality).
- Sign off on the pull request with a :thumbsup: or "Ready to merge" comment.
- Wait to merge the branch until it has passed Continuous Integration testing.
  (TDDium, TravisCI, etc.)
- Approve once you feel confident in the code and its impact on the project.

## Reviewing code

When reviewing code, you should be able to check off each of the following:

- [ ] Do the changes address the project's needs?
- [ ] Do the changes respect the project's existing style?
- [ ] Does the new code avoid reproducing existing functionality?
- [ ] Are functions as simple as possible?
- [ ] Is the code as efficient as possible?
- [ ] Is the usage of each function clear?
- [ ] Have edge cases been considered and tested for?

Use this bookmarklet code to add this checklist to your Pull Request comments:

```js
javascript:!function(){var a=document.getElementById("new_comment_field");a&&(a.value+="### Code Review Checklist\n\n\* [ ] Do the changes address the project's needs?\n* [ ]  Do the changes respect the project's existing style?\n* [ ] Does the new code avoid reproducing existing functionality?\n* [ ] Are functions as simple as possible?\n* [ ] Is the code as efficient as possible?\n* [ ] Is the usage of each function clear?\n* [ ] Have edge cases been considered and tested for?\n")}();
```

To use this as a bookmarklet:

```md
1. Bookmark this page in your browser
2. Copy the code for pullrequest.js above
3. Edit the bookmark URL and paste the copied code into the URL field
4. When you're creating a Pull Request, click the bookmark and it will insert a template for Pull Request notes and checklists into your PR.
```

### Commenting on code

When commenting on breaks to our style guide, reviewers should include a link back
to the appropriate guide.

Ex:
```
[CSS - Property Values]():

> If the value of a property is `0`, do not specify units
```

If you disagree with a guideline or there is no current guideline, open an issue in
[Insert Area]() and link back to the
discussion, rather than debating it within the review. In the meantime, follow the
existing guideline.
