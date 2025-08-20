##base model
┌─────────────┐
│  Input Data │
│ (Returns,   │
│  Covariance,│
│ Constraints)│
└──────┬──────┘
       │
       ▼
┌───────────────┐
│ Preprocessing │
│ - Covariance  │
│   shrinkage   │
│ - Black–Litter│
│ - Normalize   │
└──────┬────────┘
       │
       ▼
┌───────────────────────┐
│ Problem Formulation   │
│ - Return – λ·Risk     │
│ - Penalty constraints │
│ - QUBO encoding       │
└────────┬──────────────┘
         │
         ▼
┌─────────────────────────┐
│ Quantum Algorithm (QAOA)│
│ - Custom XY mixer       │
│ - Warm-start            │
└────────┬────────────────┘
         │
         ▼
┌───────────────────────┐
│ Quantum Execution     │
│ - Simulator/Hardware  │
│ - Measure bitstrings  │
└────────┬──────────────┘
         │
         ▼
┌─────────────────────────┐
│ Postprocessing          │
│ - Decode portfolios     │
│ - Risk parity, rebal.   │
└────────┬────────────────┘
         │
         ▼
┌─────────────────────────┐
│   Optimized Portfolio   │
│ - Asset weights         │
│ - Return, risk, Sharpe  │
└─────────────────────────┘
