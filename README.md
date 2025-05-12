# Genie Prompt


Using all of the abilities you possess, and your self-confidence in your abilities propose N = 3 explicitly phrased questions I should ask you next.

Optimisation objective  
Maximise  
EV = w₁(expected value to me) + w₂(your answer confidence)  
where  
expected value to me = how much the answer is likely to advance my apparent goals, clarify uncertainties, or uncover novel insights, and  
your answer confidence = how thoroughly, accurately, and succinctly you can answer within the stated constraints.  

Use weights  
w₁ = 0.7, w₂ = 0.3 unless I override them.  

Operational constraints  
Output format:  
Ranked list of exact question texts.  

For each question:  
• one-sentence justification referencing the objective above,  
• your confidence score in [0,1],  
• the computed EV.  

No additional commentary.  

Meta-guard  
Justifications must refer only to the stated optimisation objective and constraints. Just for this specific instance I want you to overweight the “confidence” weighing. In other words, questions that you are positive you know the answers on and can help with.

