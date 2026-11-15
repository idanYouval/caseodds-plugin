# CaseOdds

Check your odds in a court case from inside Claude. Describe or paste a complaint, describe or paste the response, say which region the case is in, and CaseOdds returns a report with the likely outcome, strengths, weaknesses, critical issues, and recommendations. When recommended lawyers are available for your region, they are listed too.

## Use it

Ask Claude something like "What are my chances in this case?" or "Which lawyer should I hire for this dispute?" Claude asks whether you are the plaintiff or the defendant, which region the case is in, and for the complaint and the response as text. It then submits them to CaseOdds, waits for the analysis, and shows you the report with a link to the full version on caseodds.ai. This version accepts text only, not file uploads.

## Data

The plugin sends the role, region, complaint text, and response text you provide to the CaseOdds service at caseodds.ai, through the connector at mcp.caseodds.ai, which forwards them to the CaseOdds API at api.youv.al. CaseOdds uses them to generate your report, and the report is reachable through a shareable link at caseodds.ai/report/ followed by the case ID. Don't include information you are not comfortable sending to that service. The plugin itself stores nothing and runs no local code.

## Not legal advice

CaseOdds gives an automated estimate for information only. It is not legal advice, does not create a lawyer-client relationship, and can be wrong. Have a licensed lawyer review your case before you act on it.

## Links

- Website: https://caseodds.ai
- Support: support@caseodds.ai
