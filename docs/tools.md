# Tools

Back to the [README](../README.md).

These are all the tools a connected assistant can use, grouped by the [permission](permissions.md)
that allows each one. You don't call them yourself: ask in your own words and the assistant picks
the tool. You may see a tool's name when your assistant asks to use it.

An assistant is only told about the tools its connection can use.

## Reading your workspace

These come with **Read flows, runs, campaigns and usage**, the one permission every connection
has. They change nothing. Phone numbers and email addresses are masked, and no messages are
included.

### For every role

| Tool | What it does |
| --- | --- |
| `get_context` | Which workspace and person this connection belongs to, what it was granted, and what it wasn't. |
| `list_conversations` | Your inbox, filtered as on the Conversations page, without the messages. |
| `list_leads` | Your leads and tags, filtered as on the Leads page. |
| `list_meetings` | The meetings on your Send4 calendar. |
| `find_meeting_times` | The free times for a customer, or the times a meeting could move to. Nothing is booked. |
| `list_members` | The people in your workspace. A Client Admin sees their details, and anyone else sees names. |
| `list_channels` | Your sending numbers and mailboxes, and whether a campaign can send from each. |
| `get_performance` | Conversations started, replies, details collected, bookings and cost over time. |
| `get_message_usage` | Messages and SMS parts sent and received, their cost, and your monthly SMS limit. |

### For Client Admin and Client Agent

| Tool | What it does |
| --- | --- |
| `list_flows` | Your flows, with their status and what starts them. |
| `read_flow` | One flow in full, with its cards, settings and wiring. |
| `check_flow` | Everything the flow builder would flag on a flow. |
| `list_card_types` | Every type of card a flow can use. |
| `describe_card_type` | What one type of card does and which settings it takes. |
| `get_flow_building_guide` | Send4's rules and common traps for building a flow. |
| `list_flow_templates` | The ready-made flows a new flow can start from. |
| `list_personas` | The identities a flow's AI can speak as. |
| `list_flow_runs` | The runs of one flow and how each ended. |
| `get_flow_health` | How many runs of a flow started lately and how they ended. |
| `get_drop_off` | Where conversations stop, across your flows or card by card in one. |
| `explain_conversation` | What happened in one conversation or flow run, which cards it went through, and what's still missing. |
| `compare_card_text` | How new wording differs from a card's current text. Nothing is saved. |

### For Client Admin only

| Tool | What it does |
| --- | --- |
| `get_account_usage` | What you've used against your plan in a month. |
| `list_campaigns` | Your campaigns, with their status and results. |
| `read_campaign` | One campaign's status, progress and results. |
| `get_campaign_report` | A launched campaign's report, by card, day and meeting. |

## Reading customer messages

This comes with **Read conversation messages**. With this permission, `list_conversations`,
`list_leads` and `list_meetings` also show customers' names, and `explain_conversation` also shows
recent messages and the details collected. Contact details stay masked.

| Tool | What it does |
| --- | --- |
| `read_conversation` | What was said in one conversation. Every role. |

## Building flows

These come with **Build and change flows**, for a Client Admin. None of them can change a live
flow. Instead, the assistant duplicates it, changes the copy and rehearses it. Switching the copy
on and the original off then needs your yes.

| Tool | What it does |
| --- | --- |
| `create_flow` | Start a draft flow, blank or from a template. |
| `duplicate_flow` | Copy a flow into a new draft. The copy gets its own webhook address, so anything that sends to the old one has to move. |
| `edit_flow` | Change a draft or switched-off flow: its cards, where each one leads, what starts it, its name and its settings. All the changes are saved together or not at all, and the answer reports anything they broke. A live flow can only be renamed. |
| `save_persona` | Create or change a persona. A persona used by a live flow can't be changed. |
| `suggest_card_change` | Leave new wording on one card for a person to accept in the builder. It changes nothing live, so it works on a live flow too. |
| `rehearse_flow` | Play a flow as the customer on Send4's simulator. Nobody is texted, but webhook, email and Hanna cards still send for real, marked as tests. |
| `read_rehearsal` | Read what was said in a rehearsal. |
| `preview_flow_status` | See what switching a flow on, or a live flow off, would do, without doing it. Send4 gives the assistant a summary to show you and ask for your yes. |
| `set_flow_status` | Switch a flow on or off. Switching one on, or a live one off, needs the code from that preview. |

## Running campaigns

These come with **Create and launch campaigns**, for a Client Admin on a plan with campaigns.

| Tool | What it does |
| --- | --- |
| `preview_campaign_audience` | Count who a campaign would reach, before creating it. |
| `create_campaign` | Create a draft campaign. Nothing is sent. |
| `preview_campaign_launch` | Run every launch check and work out the cost, without sending anything. Send4 gives the assistant a summary to show you and ask for your yes. |
| `launch_campaign` | Send a draft campaign to its recipients, using the code from that preview. |
| `preview_added_recipients` | Count who would be added to a campaign, without adding anyone. Send4 gives the assistant a summary to show you and ask for your yes. |
| `add_campaign_recipients` | Add those people to the campaign, using the code from that preview. On a running campaign, they'll be messaged. |
| `update_campaign` | Change the pace, sending hours or goal of a campaign that's scheduled, running or paused. |
| `pause_campaign` | Stop starting new people. Conversations already going carry on. |
| `resume_campaign` | Start new people again. |
| `cancel_campaign` | Stop a campaign for good. A draft is deleted. |
| `create_lead` | Add one lead. This sends nothing. |
| `tag_leads` | Add tags to leads or take them off. |

## Working the inbox and calendar

These come with **Reply to customers and manage conversations**, for every role.

| Tool | What it does |
| --- | --- |
| `send_message` | Reply to a customer. Once sent, it can't be taken back, and the AI stops answering that conversation. |
| `preview_new_conversation` | Check how a typed phone number reads and the exact text, without sending anything. Send4 gives the assistant a code for it. |
| `start_conversation` | Text someone first. A typed number needs the code from that preview; a lead doesn't. Once sent, it can't be taken back, and no flow answers until the AI is resumed. |
| `assign_conversation` | Give a conversation to a team member, or to nobody. The AI keeps answering. |
| `take_over_conversation` | Pause the AI so a person answers. |
| `resume_ai` | Hand a paused conversation back to the AI. |
| `mark_lead_opted_out` | Stop texting a number, for a customer who asked in words other than STOP. Only a person can opt it back in, on the lead's page. |
| `book_meeting` | Book or move a meeting. This doesn't tell the customer. |
| `update_meeting` | Cancel a meeting, or mark it completed or a no-show. A cancellation tells the customer only if the assistant is asked to. |

## Managing your team

These come with **Invite and manage team members**, for a Client Admin.

| Tool | What it does |
| --- | --- |
| `preview_member_invite` | See who would be invited, in which role, and the seats in use, without sending anything. Send4 gives the assistant a summary to show you and ask for your yes. |
| `invite_member` | Invite someone as a manager or agent, using the code from that preview. Nobody can be made an admin this way. |
| `update_member` | Change someone's role between manager and agent, or deactivate or reactivate them. |
| `resend_invitation` | Send a fresh link to someone whose invitation is still pending. |

## Setting up email

These come with **Create email addresses**, for a Client Admin.

| Tool | What it does |
| --- | --- |
| `get_mailbox_setup` | Whether this workspace can have an email address on Send4 and on which domains, whether it can connect its own mailbox, and the Send4 page that does it. |
| `create_mailbox` | Create an email address on Send4. It sends nothing until a flow or a campaign uses it. |

No tool takes a mailbox password. To connect your own mailbox, use the page `get_mailbox_setup`
links to.

## Used by the in-chat views

This one isn't offered to the assistant. The flow map that some assistants show in the chat calls
it to redraw a flow while it's on screen.

| Tool | What it does |
| --- | --- |
| `get_flow_map` | Draw one flow card by card, for the flow map view. |

## Ready-made requests

Some assistants also offer these as commands. Each one is only a request to the assistant, so it
can't do more than the tools above allow.

| Request | What it does |
| --- | --- |
| `weekly_report` | A short report on conversations, replies, bookings, campaigns and where people drop off. |
| `explain_conversation` | Where a conversation's flow stopped or went off course, and why. |
| `build_flow_from_brief` | Turn a description of a flow into a draft, checked and rehearsed. |
| `check_campaign_before_launch` | Go through a draft campaign and list what to fix before it goes out. |
