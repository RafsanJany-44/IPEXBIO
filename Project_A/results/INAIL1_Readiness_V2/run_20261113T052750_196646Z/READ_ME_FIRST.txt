Project A INAIL1 readiness V2

{
  "version": "2.0",
  "project_root": "/home/rafsan/Documents/GitHub/IPEXBIO/Project_A",
  "data_root": "/home/rafsan/Downloads/INAIL_1/Dataset1/DATA",
  "participants_loaded": 17,
  "trial_rows": 132,
  "parser_issues": 0,
  "structural_candidates": 121,
  "cross_subject_quarantined_trials": 2,
  "duplicate_event_conflict_trials": 6,
  "documented_alignment_trials": 0,
  "reviewed_target_rows": 0,
  "mvc_channels_flagged_ratio_gt2": 3,
  "INAIL2_decision": "Not required to resolve INAIL1. Consider compatible external validation after valid INAIL1 targets and within-condition added value are established.",
  "timing_conclusion": "Hypotheses inspected; only evidence-backed reviewer entries bound to source hashes can change documented timing status.",
  "training_status": "not_trained",
  "next_action": "Inspect duplicate provenance, timing/source exports and MVC plots; resolve the ledger before model development."
}

Primary outputs: trial_inclusion_ledger.csv, channel_inclusion_ledger.csv, duplicate_provenance.csv, mvc_channel_review.csv, protocol_extraction.json and figures.

No training performed. Candidate normalization is filtered RMS based and needs contraction/unit review. Current snapshots preserve all source records. Across-participant duplicated signal trials are quarantined. Duplicate event conflicts are held. No evidence-free offset is selected.

Review templates: set evidence and reviewer only after actual source verification. emg_offset_s is added to movement elapsed seconds. source hashes must match. Reference method is fixed to max_filtered_rms_p95_250ms. Rerun V2 with explicit review-file configuration paths.

All outputs remain under PROJECT_ROOT/results/INAIL1_Readiness_V2. Archive contains diagnostic tables, protocol text, participant descriptors and figures but no raw MATLAB/TDF arrays.