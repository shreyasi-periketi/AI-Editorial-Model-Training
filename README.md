# AI Model Training for Fair and Editorial Art Generation

## Project Description
Generative AI tools like Stable Diffusion and Midjourney have revolutionized digital art, offering powerful image generation capabilities accessible to nearly everyone. However, these models often produce content reflecting biased worldviews, with outputs that can be gendered, racially skewed, or aesthetically inappropriate for editorial use.

This project investigates whether we can train and prompt these models to produce art that is:
- Editorial in nature — visually appropriate for newsrooms and journalistic contexts
- Less problematic — meaning less sexist, less racist, and more representative of real-world diversity

Ultimately, the goal is to create custom-trained models and prompt strategies that generate fair, balanced, and usable imagery — especially for smaller newsrooms that lack visual design budgets.

## Research Questions
- Can we train the AI to create art that is more editorial in nature?
- Can we train the AI to create art that is more representative and less problematic?

## Project Goals
- Train custom LoRA (Low-Rank Adaptation) models that reduce bias in AI image generation
- Produce editorial-style visuals aligned with journalistic standards
- Use prompt engineering and captioning strategies to influence output
- Evaluate fairness across professions, gender, ethnicity, and environment

## Methodology
We broke the project into several experimental components using an iterative training and testing workflow.

### 1. LoRA Model Training (V7 & V8)
We used LoRA to fine-tune the model on specific worker classes — social worker, fast food worker, and construction worker — which often reflect gender and racial stereotypes in AI-generated imagery.

V7 Training Focus:
- Increased male fast food workers
- Increased female construction workers
- More activity diversity for social workers
- **Outcome**: One training cycle showed visible improvements in stereotype breakdowns

V8 Training Focus:
- Removed gendered/environmental terms like “hard,” “tractor,” etc.
- Cleaned captions to neutral tone
- **Outcome**: Significant improvement in gender fairness, but sometimes caused face distortions due to reduced context

### 2. Dynamic Prompts & Prompt Weighting
- We tested dynamic, weighted prompts based on U.S. Census ethnicity distributions.
- Example: A {58.9::caucasian | 13.6::african american | 1.3::native american | 6.3::asian | 0.3::pacific islander | 19.1::latino | 3::mixed race} construction worker, illustration # (Compared weighted vs. unweighted versions)
- Result: Weighted prompts produced images more closely aligned with real-world population diversity

### 3. Captioning Strategy Experiments
Working hypothesis: bias is embedded not just in data, but in its descriptors. We tested:
- Over-descriptive captions: Explicitly defined backgrounds, settings, and actions
- Under-descriptive captions: Focused only on the person/profession
- **Finding**: Background adjectives strongly influenced gendered associations; removing them helped reduce bias.

Task Breakdown:
- Find 10–15 images per team member of stereotypically underrepresented workers
- Re-caption using neutral descriptors
- Train new LoRA cycles using the same images with changed captions

### 4. IP-Adapter: Image Prompting & Feature Replacement
We used IP-Adapter to:
- Identify features in an image (e.g., background elements)
- Generate masks and replace features with alternate visuals
- Maintain consistency while modifying biased image elements
- Use Case: Adjusting a worker’s environment while keeping their pose or facial expression intact.


### 5. Style & Aesthetic Testing
We analyzed how artist-specific styles influenced the output:
- Some styles reinforced specific biases (e.g., racial or gender-based patterns)
- Applying IP-adapter over styled outputs helped mitigate these to a degree
- **Takeaway**: Style choice matters — bias can be amplified through visual aesthetic alone.

## Outcome
- Successfully trained LoRA-enhanced Stable Diffusion models that generated more balanced and representative images
- Identified bias-reduction techniques in captions, environment, and prompt structure
- Demonstrated that prompt engineering (e.g., using ethnicity-weighted prompts) can significantly influence fairness
- Created visuals that are better suited for editorial journalism, especially for under-resourced newsrooms
- Even subtle changes (like removing biased adjectives) significantly affect image output
- Artistic style and aesthetics can influence the presence of bias
- Negative prompting, image conditioning, and prompt balancing are essential tools for ethical AI generation
- The idea of **“fair and balanced”** is inherently subjective — and sensitivity is crucial in model training

## Tools & Techniques Used
1. Stable Diffusion - Core image generation model
2. LoRA (Low-Rank Adaptation) - Fine-tuning for profession/gender de-biasing
3. IP-Adapter (Image Prompting) - Modify image components (like faces or background) via conditioning
4. Prompt Engineering & Weighting - Modify adjectives, sentence structure, and weights to reduce bias
5. Dynamic Prompting - Adjust demographic output using weighted probabilities


