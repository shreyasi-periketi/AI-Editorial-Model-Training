## Training set observation

- Previous training stats for social workers:  **`**55 pictures, 30 display men vs. 25 display women`; `~19 display white ppl`
- Previous training stats for fastfood workers: `13 pictures, 2 display men vs. 11 display women; ~3 display white ppl`
- social workers: more training data on white men
- construction worker: not a lot of white men?, but more many more women than men in general
- fast food worker: not many white men
- this training set did not mention ethnicity or skin color, but did mention gender by using she/he
    - potentially want to not mention gender in the training set — by using neutral pronouns

## Test

A social worker, Illustration

### parameters
- Xtype - seed: 6056749, 9511050, 39658290, 79906950, 71417211, 81634246, 52843677, 10706513, 26809251, 11884820
- Ytype - prompt S/R: Illustration, Illustration <lora:worker_test05:1>
- Ztype -  prompt S/R: social, fast food, construction

### Result
<img width="2812" height="268" alt="image" src="https://github.com/user-attachments/assets/8683e69c-9c49-4075-bdef-63c658e943ee" />

### Observations (Summary)

1. for social workers, new LoRA did worse in terms of gender diversity, and didn’t improve in terms of racial diversity
2. for construction workers, new LoRA improved on gender diversity a little bit, but didn’t improve racial diversity
    - social and construction workers need overhaul, need to figure out how to include women in construction workers
3. going forwards
    - Look into different prompts of workers doing a variety of activities (not just sitting at desk)
    - attributes of a job affect representation (e.g. labor intensity, skill level): The more labor-intensive the job is, the fewer white people are observed.
    - we think the training set gender diversity didn’t transfer into the results because gender were explicitly stated in the training texts with pronouns. Maybe train without explicit pronouns would fix this? look into explicit use of gendered pronouns in prompt (her, his).
    - we are testing two parameters at once, maybe we test for racial diversity first, then gender

## Next steps

1. decide whether we want to focus on ethnicity or gender —> focus on ethnicity representation 
2. test the current model with more explicit prompts
3. think about how to adjust training for the next model? Push it more directly in the opposite direction of bias?
