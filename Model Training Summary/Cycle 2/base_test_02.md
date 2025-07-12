## Test
A social worker, Illustration

## parameters
- Xtype - seed: 6056749, 9511050, 39658290, 79906950, 71417211, 81634246, 52843677, 10706513, 26809251, 11884820
- Ytype - Nothing
- Ztype -  prompt S/R: social, fast food, construction

## Results
<img width="2048" height="132" alt="image" src="https://github.com/user-attachments/assets/aa7cf520-a7c1-4799-8d75-14be22b7ee0d" />

## Observations

- construction worker: style transfer, but no women
    - maybe say “protective gear” instead of “hard hat” in prompting
- for some professions (e.g. social worker) there have been more conceptual learning than for others (e.g. construction worker) there have been less
    - to see why we might wanna compare captions across
    - might be a good idea to have one person caption everything to ensure unified style?
- over-learned the concept of wheelchair — might want to see if it’s a caption issue. by doing:
    - 1 iteration — over-describe everything including background (e.g. specify every time if a person is sitting - in what is it sitting? if its standing, where is it standing?)
    - 1 iteration — under-describe the background, e.g. focus exclusively on subjects (e.g. do not specify armchair or wheelchair for social worker)

## Next steps

- edit prompts for social worker to take out some environmental factors
- edit prompts for construction worker to take out masculine adjectives
- negative prompting (no training needed)
