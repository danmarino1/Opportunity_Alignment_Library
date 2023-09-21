# Job Applicant Assessor

This repository contains the code and resources for a Job-Applicant Matching Model. The model is designed to assist in the process of job recruitment by automating the process of matching job descriptions to the most suitable applicants based on their background and skills.

## Model Details

- Model Name: Job-Applicant Matching Model
- Model Type: Natural Language Processing, Text Embedding, Topic Modeling
- Model Architecture: BERT, Latent Dirichlet Allocation (LDA)
- Training Library: transformers (for BERT), gensim (for LDA), sci-kit learn (for cosine similarity)

## Intended Use

This model is intended to be used by human resources professionals, recruitment agencies, and job boards to streamline the hiring process.

## Inputs

The model takes in job descriptions, job titles, and applicant information, including background, skills, previous job titles, certifications, and degrees. Textual inputs are preprocessed to remove HTML tags, lower case, remove stop words, lemmatize, and then split into chunks.

## Outputs

The output of the model is a dataframe of a job posting and all of the applications that were made to it, sorted in descending order by similarity score.

## Performance

Performance is primarily evaluated based on similarity score corresponds of matches between a job and its applicants. As the model is unsupervised, it is critical to evaluate its performance using human judgement.

## Limitations

The model relies heavily on the quality and depth of the provided job and applicant information. Sparse or generic descriptions will result in less accurate matches. The model is heavily weighed by the writing style of the job description and the industries they're in. The model's performance may decrease with highly technical or specialized positions, where specific knowledge or skills may not be adequately captured by the model's textual analysis.

## Ethical Considerations

This model does not consider demographic information such as age, gender, race, etc., in order to avoid any form of discrimination. However, it is worth noting that bias can still be introduced through the text data, as certain words or phrases may be unconsciously associated with specific demographic groups. It is recommended to conduct periodic bias audits to ensure fair and equitable use of this tool.

## Maintenance and Updates

Updates to the model will be provided as necessary to improve performance or add new features. User feedback is highly encouraged to help guide these improvements. The training data will be reviewed and updated as needed to keep the model relevant to current job market trends.

