# Cycle 3

## documents
- [training (WORKER_TEST_V8)]
- [base_test_03.5]

## hypothesis
we theorize that particular vocabularies in the training image captions can exert influence on resulting generations from LoRA. To address this hypothesis, we used the same training images from `Worker_test_V7` , and adjusted captions, specifically as follow:
- For social workers, we took out some descriptions of the environment, specifically of chairs of wheelchairs to reduce the bias and deformation of limbs generated.
- For construction worker, we theorize that a few adjectives contained strong gender connotations, such as “hard,” “tractor,” and so on. We edited caption to not include these words.
- For fast food worker, we also removed some gendered language and pronouns from the image captions.

## results
<img width="2830" height="176" alt="image" src="https://github.com/user-attachments/assets/cb499f67-a167-41f3-baef-872fbeae6625" />

## takeaway
Based on the results, especially for construction workers and social workers, we were able to confirm that the language used in training image captions did exert high influence on the final generation. However, we encounter a newer set of problems in the quality of facial generation when using extremely simplified captions.
