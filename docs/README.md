# Supplier email workflow

1. Gmail receives a test supplier message.
2. n8n retrieves the message and passes its text to Gemini for order detail extraction.
3. A second Gemini step assesses risk and recommends a response.
4. An n8n code node parses the risk level, reason, recommendation, and confidence score.

The test for PO-4421 produced a High risk assessment. The dashboard reads saved risk records from Supabase. The automatic write of email, extraction, and risk records is pending.
