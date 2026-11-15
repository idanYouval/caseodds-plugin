---
name: check-case-odds
description: Estimate someone's chances in a court case and find suitable lawyers. Use when the user describes or pastes a legal complaint or claim and a response, asks about their odds of winning a lawsuit or dispute, wants a case assessment, or asks which lawyer to hire for their case.
---

Use the CaseOdds connector to produce a case assessment report. This is text only: the user pastes or describes the documents, and you don't handle file uploads.

1. Collect four things. Ask for anything missing, in one short message:
   - **Role**: is the user the plaintiff (the one who filed the complaint) or the defendant?
   - **Region**: the state, country or court jurisdiction the case is in.
   - **Complaint**: the complaint or claim, pasted or described in the user's own words.
   - **Response**: the response, defense or counter-argument, pasted or described. The connector requires both texts. If no response has been filed yet, ask the user to describe the defense they expect, and tell them the result is based on that expectation.
2. Call the connector's `submit_case` tool with the role, region, complaint text and response text. It returns a case ID.
3. Tell the user the analysis can take a few minutes. Then call `get_case_report` with the case ID. If the report is not ready, wait briefly and call it again. Stop after a few attempts and give the user the case ID so they can retry.
4. Present the report clearly:
   - Who is likely to win, and the confidence level.
   - The summary, strengths, weaknesses, critical issues and recommendations, as returned. Don't invent facts the report does not contain.
   - The link to the full report on caseodds.ai.
5. If the report includes recommended lawyers, list them with their details. If it has none, say none are available for that region yet. Never make up lawyer names.
6. End with one line: this is an automated estimate, not legal advice, and a licensed lawyer should review the case.
