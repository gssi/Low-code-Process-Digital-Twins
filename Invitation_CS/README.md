## Invitation CS

In the **Invitation CS**, the user interacts with the invitation process through web-based forms **(d)** providing the required data (we blurred the sensible data due to privacy).

To visualize in real-time the state of an invitation, the information system supports the dashboard **(c)**. A pie chart, for instance, shows the distribution of the invitations in real-time, allowing users to analyze the invitation process at a glance and make data-driven decisions about process improvements if needed.

The [Figure](https://github.com/MT91/Low-code-Process-Digital-Twins/blob/main/Invitation_CS/Invitation%20CS.pdf) **(a)** shows the implemented workflow managing the status of the system and the process. The initial trigger node checks iteratively when a new guest invitation is opened on the Notion database, which is used as an information system and extracts some additional information with intermediate nodes. Then, a *Switch* node checks the system's current status and routes the process accordingly. 

![Figure](Invitation_CS.png)
The system automates several steps, such as monitoring new entries in the Notion database, generating invitation letters, attaching them to emails, and updating statuses from the invitation start, passing by confirming the activities carried out to the reimbursement. These automation elements reduce manual intervention, enhancing the process's efficiency. For instance, the top branch will check if all required information is provided in the Notion record and then start creating the invitation letter needed to attach to the email to the guest. When this top branch is terminated, the system's status, particularly of the subject invitation, is changed to the next status of the process, i.e., from *invitation Ready to be sent* to *Invitation sent*.

The status change of the invitation process is not only automatically changed by the system (as can be seen by the login **(e)**) but also by the users interacting with the information system, e.g., changing manually the status of the invitation from *Draft* (not finalized) to *Started* to *Ready to be sent*. The system will interpret manual status changes at the next workflow run, in which the switch node will evaluate the new status, and so on. A video demo is available [here](https://www.youtube.com/watch?v=OhRlFIM9uhA) where an automatic and a manual change of status are shown.

[![Figure](https://github.com/gssi/Low-code-Process-Digital-Twins/blob/main/COBOL_CS/image_2024_11_29T10_26_52_556Z.png)](https://www.youtube.com/watch?v=OhRlFIM9uhA)
