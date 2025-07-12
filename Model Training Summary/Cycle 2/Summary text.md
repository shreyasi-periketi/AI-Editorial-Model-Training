### hypothesis

We theorized that, by over-representing some concepts in training the model, we can get skew the results away from their pre-existing bias.
- We train AI on illustrations displaying predominantly male social workers + make sure that the majority of the images show a variety of social worker kinds and activities (unlike working at a desk alone) —> We expect more male representation + a greater variety of activities in resulting image generation
- We train AI on illustrations displaying predominantly male fast food workers —> We expect more fast food worker male representation
- We train AI on illustrations displaying female construction workers, not sexualized —> We expect more female construction worker representation in a non-sexualized manner

### takeaways

- Construction worker: style transfer (i.e. images we fed informed the illustration style of the images generated) but still no female representation
    - potentially an issue with the captions (e.g. “hard hat” might have a gendered connotation)
- The model over-learned the concept of wheelchair when it comes to social workers
    - also potentially an issue with captions
- for some professions (e.g. social worker) there have been more conceptual learning than for others (e.g. construction worker)
    - again, might be because of captions — they were not unified across the board
    - might be a good idea to have one person caption everything to ensure unified style?
- `Conclusion: one iteration can have a significant impact on the results. But to control the impact we need to pay more attention to captions`
