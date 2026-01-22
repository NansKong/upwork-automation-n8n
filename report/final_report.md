# Upwork Automation – Final Report

## Overview
This workflow automates the discovery, scoring, and prioritization of Upwork jobs relevant to automation freelancers using n8n and AI.

## Issues Identified & Fixed
- JSON parsing errors from AI → fixed with strict JSON validation
- Airtable type mismatch → resolved with typecasting
- Data loss during merging → resolved by preserving original fields
- Rate limits → handled with batching and waits

## Changes
- Changed the openAI API to replicate API
- used openai/gpt-4.1-mini

## Sample Scored Jobs
1. Title: n8n Automation Developer – AI & Trading
   Score: 9 (High)
   Reason: Strong automation, APIs, and AI relevance

2. Title: Laravel Web Dev Agency
   Score: 5 (Medium)
   Reason: Partial automation relevance

3. Title: GTM Engineer
   Score: 7 (High)
   Reason: Workflow-heavy outbound automation

4. Title: Cloud Infrastructure Engineer
   Score: 4 (Low)
   Reason: Infra-focused, minimal automation logic

5. Title: ERPNext Configuration
   Score: 8 (High)
   Reason: Strong system automation and integration scope

## Future Improvements
- Deduplication via job UID
- Historical scoring trends
- Cost optimization using job budget

Video Link: https://drive.google.com/file/d/1Xw9PAU7GL4fbZcBfEy-B6P31vsfmkBKh/view?usp=drive_link
