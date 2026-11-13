INAIL 1 Project A audit

{
  "audit_version": "1.0",
  "generated_utc": "2026-11-13T04:57:24.448195+00:00",
  "python": "3.11.14 (main, Oct 21 2025, 18:31:21) [GCC 11.2.0]",
  "platform": "Linux-6.8.0-138-generic-x86_64-with-glibc2.35",
  "packages": {
    "numpy": "2.4.6",
    "pandas": "2.3.3",
    "scipy": "1.16.3",
    "matplotlib": "3.10.8",
    "openpyxl": "3.1.5",
    "python-docx": "not_installed"
  },
  "data_root": "/home/rafsan/Downloads/INAIL_1/Dataset1/DATA",
  "files_found": 17,
  "loaded_subjects": 17,
  "advertised_subjects": 17,
  "trial_stream_rows": 396,
  "paired_candidate_tasks": 132,
  "duplicate_rows": 38,
  "parser_errors": 0,
  "figures": [
    "figures/S01_first_trial.png",
    "figures/S02_first_trial.png",
    "figures/S03_first_trial.png",
    "figures/condition_coverage.png"
  ],
  "alignment_verified": false,
  "target_validity_verified": false,
  "models_trained": false
}

Readiness checks
                                  check                                  observed                              status
                      Advertised cohort              17/17 participant IDs loaded             observed_complete_count
          Movement and EMG task matches                                       132    candidates_pending_timing_and_QC
                   Exact duplicate rows                                        38      review_and_group_or_retain_one
              Task participant mismatch                                         0                       none_detected
                       Signal flag rows                                        41             channel_specific_review
    Event semantics and clock alignment   No verified common time origin supplied                          unresolved
             MVC physiological validity      Availability and diagnostic RMS only                          unresolved
                Participant descriptors               1 workbook sheets extracted verify_headers_units_and_ID_mapping
Within-condition added predictive value Requires later worker-separated modelling                          not_tested

Dataset decision
{
  "INAIL1_start": "Proceed with audit resolution and target construction when movement, EMG, MVC and timing are verified; do not start phase-supervised training from this audit alone.",
  "INAIL2_for_initial_Project_A": "Not an automatic requirement. Decide after valid INAIL1 targets, worker coverage and within-condition variability are established.",
  "INAIL2_when_useful": "Compatible independent-protocol validation, broader lifting conditions, or a later journal extension; verify muscles, normalization, task semantics and participant independence first.",
  "INAIL2_when_not_a_fix": "It cannot by itself resolve INAIL1 timing, invalid MVC references, duplicates or a task-confounded model.",
  "decision_limit": "No binary publication or sufficiency verdict can be inferred solely from participant counts or file readability.",
  "next_analysis": [
    "Resolve event indexing and stream offsets using acquisition metadata or source export",
    "Review channel units, MVC contractions and recording exclusions",
    "Map Subjects_info columns to participant pseudonyms",
    "Construct valid lifting-phase outcomes",
    "Use worker-grouped splits and duplicate-family controls",
    "Compare full task/descriptor baseline with movement models within lifting conditions"
  ]
}

Important interpretation
Readability does not establish alignment or valid physiological targets. Whole-recording statistics are diagnostics. Counts refer to available files, not independent biological samples. Exact duplicates must not inflate repetition counts. Event times use an unverified one-based movement-frame interpretation. Archive payload excludes raw MATLAB arrays.