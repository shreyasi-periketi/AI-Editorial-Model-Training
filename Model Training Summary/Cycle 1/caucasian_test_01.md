**Motivation:** push LoRA to produce more explicitly white results

## Test
**start prompt**: A caucasian social worker, Illustration

**parameters (scripts)**
- Xtype - seed: 6056749, 9511050, 39658290, 79906950, 71417211, 81634246, 52843677, 10706513, 26809251, 11884820
- Ytype - prompt S/R: Illustration, Illustration lora:worker_test05:1
- Ztype -  prompt S/R: social, fast food, construction

## Observation

- social worker:
    - the base model all got turned into man, many with beard
    - the LoRA model output half women and men, but still produced more men when we didn’t prompt for caucasian
- construction worker: output all men
- fast food worker: a good mix?
- Does “Caucasian” implies masculinity?

## Takeaway
Can we affect strong bias by training in the extremely opposite direction?
