## Project Lifecycle

At Expertizo, all tasks are created as tickets through [Trello](https://trello.com/).

If a ticket is classified as a Project, the following steps take place:

1. The Task is assigned to a development team or a developer by the Engineering Manager or Project Manager. 
2. Assigned developer(s) creates an estimate ([this is a good resource for generating estimations](https://jacobian.org/2021/may/25/my-estimation-technique/)) of the work involved. The creation of this estimate will usually have a deadline assigned by the Engineering Manager or Project Manager, but should usually be done as soon as is pracitcal given other work priorities.
3. Developer(s) post the estimate to the `#general` channel using the Geekbot standup following format:

> **What is your plan till day end?**: 
* [I will fix the scroll bug on Contact Us Page](https://trello.com/c/PpZs436F/18-edit-short-not-working)
* [I will integrate forgot password API](https://trello.com/c/PpZs436F/18-edit-short-not-working)
> 
> **Provide estimations for each of the above tasks mentioned.**:
* 3 hrs
* 2 hrs
> 
> **Anything blocking your progress?**:
* Forgot password API isn't working anymore.
> 

4. Follow the [Workflow](./gitAndGitHub.md#workflow) process to complete the Project.

5. [Documentation](./projectDocumentation.md) must be added or updated in the repository for this Project's code.

### Planning Document
In order to facilitate proper forethought and planning in a project, a planning document should contain the following, at a minimum:
* Introduction which identifies the problem/task to be solved, along with relevant context.
* Presentation of at least three engineering approaches to solve the problem/task.
* After the presentation of each approach, the pros and cons of each approach should be listed so the approaches can be compared.
* A summary in which the chosen approach is identified, along with a logical explanation for its selection.
* Any other relevant information explaining the estimate or project details.

### Additional Note
* Tickets marked with the label `Urgent` bypass this process and should be worked on immediately.
