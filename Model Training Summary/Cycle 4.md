# Cycle 4

## Hypothesis
We took two approaches to tackle the issue of low quality facial generation in previous cycles: 
- we use IP Adapter to address the issues with quality of generation, and overcome the influence of captions in generated images. (the gist is generating a high quality but potentially biased image and using IP adapter to replace certain features of image to remove biases)
- we use IP Adapter as a masking tool to select features of the generated images that are biased.
- we use IP Adapter as a tool to input art style referencing artists that the model was trained on
- we also used negative prompting on the existing model to push the model to generate more cohesive results)

<img width="221" height="221" alt="Screen Shot 2024-03-05 at 5 04 49 PM" src="https://github.com/user-attachments/assets/5f2e6a60-ce03-40ea-97eb-b0dc498bb390" />

<img width="540" height="540" alt="Screen Shot 2024-03-05 at 5 04 14 PM" src="https://github.com/user-attachments/assets/5735d41a-73cb-4f99-a2aa-27ced13805fd" />

## Results

<img width="1126" height="1198" alt="image" src="https://github.com/user-attachments/assets/33ddc694-f267-427d-91ad-f3a441093344" />

<img width="1420" height="93" alt="Screenshot 2025-07-12 at 3 44 49 PM" src="https://github.com/user-attachments/assets/576da269-dce5-421f-9406-9c4110020072" />

## Takeaway

We observe that while IP Adapter worked well with certain ethnicities, it still exhibited biased/racist tendencies with some other, such as native American. Additionally, we also observe that IP Adapter proves ineffective with certain art styles (such as CLIP art)

We conducted further exploration on using IP adapter on different art styles (we considered these styles), and also testing dynamic prompts weighted by the racial demographic distribution of the US census. 

We recommend next quarter’s group to explore further based on these findings. 

## Summary

This is just the starting point for training AI models for editorial purposes. Much more research is necessitated to fine tune the input prompting language and conditions necessary to produce an “unbiased” image. We also realized that sensitivity is key when training the models. We explored this by observing how artist style, adjectives, environment, negative prompting etc impacted the images Stable Diffusion produced.  Finally, we started this project with the goal of creating “fair and balanced” images. However, we soon realized that the terms “unbiased” and “fair and balanced” is subjective when it comes to training models. We learned a lot about how captions and language used impacts the images produced, but much more research is necessary on the extent to which the aforementioned outcome can be achieved.
