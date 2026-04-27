# INFER Study Alpha — Treatment Group 1

## Study Condition: INFER chain prompt + Tutorial Video

This is the **Treatment 1** version of the INFER 4-video experiment.
Participants receive INFER chain-prompt feedback on Videos 2 & 3, and additionally watch a tutorial video before Video 2 explaining how to use the INFER feedback.

### Video Configuration

| Video | Tutorial | INFER Feedback | Notes |
|-------|----------|----------------|-------|
| Video 1 | ❌ | ❌ | Reflection only (baseline) |
| Video 2 | ✅ | ✅ chain | Tutorial first, then chain-prompt INFER feedback |
| Video 3 | ❌ | ✅ chain | Chain-prompt INFER feedback |
| Video 4 | ❌ | ❌ | Reflection only (post-test) |

### Study Flow

```
Welcome/Consent → Login → Pre-Survey (mandatory)
    ↓
Video 1: Watch → Reflect → Submit → Post-V1 Survey
    ↓
Video 2: Watch → [Tutorial Video] → Reflect → INFER chain feedback → Revise → Submit → Post-V2 Survey
    ↓
Video 3: Watch → Reflect → INFER chain feedback → Revise → Submit → Post-V3 Survey
    ↓
Video 4: Watch → Reflect → Submit → Post-V4 Survey
    ↓
Post-Survey (mandatory) → Thank You
```

### Difference from Beta and Gamma

- **vs Beta (Treatment 2)**: Alpha shows a tutorial video before Video 2; Beta does not. Both use the same INFER chain prompt.
- **vs Gamma (Control)**: Alpha uses the INFER chain prompt — binary classification of every reflection window into Description / Explanation / Prediction, then a weighted feedback prompt over those analysis results (max_tokens=2000). Gamma uses a single-shot general prompt with no classification.

### Deployment

Static site on Render. URL: `infer-study-alpha.onrender.com`
Data: shared Supabase project (distinguished by `treatment_group = 'treatment_1'`).
