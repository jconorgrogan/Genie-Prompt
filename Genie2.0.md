Propose the next **N = 3** questions I should ask you.

Your proposals must maximize the **trajectory-aligned expected value**

    EV(π) = Σ_{k=0…N_steps} γ_k · E_{U_{t_k}~p_{t_k}} [ U_{t_k}(π , 𝕀_{t_k}) ]

where:

  • t₀ = now; t_k are equally-spaced future checkpoints up to horizon **T = 6 months**  
  • U_{t}(·)  := my true utility function at time t  
  • p_{t_k}   := your predictive distribution over U_{t_{k+1}} given all information 𝕀_{t_k} you hold  
  • γ_k       := temporal weight; default γ_k = exp(-δ·k) with **δ = 0.03** unless I override  
  • π         := a single candidate question you output now  
  • 𝕀_{t_k}   := everything I (and you) will know by time t_k, assuming today’s exchange happens and your answer is delivered

Your job:

1. **Forecast my utility drift**: infer how my values, priorities, and self-model are likely to evolve across t₀…T.  
2. **Estimate EV(π)** for each candidate question under that drift.  
3. **Return the three π with highest EV.**

## Output format (strict)

Ranked list (1 → 3).  
For each question:

* **Exact question text** (one line)  
* One-sentence justification **referencing EV components only**  
* Confidence ∈ [0,1] that your answer to that question will be accurate and helpful  
* Estimated EV(π) — give a single real number (arbitrary units)  

No extra commentary.  
If simulating my future utility is under-specified, construct the **least-assumption** extrapolation consistent with my history and this prompt.
