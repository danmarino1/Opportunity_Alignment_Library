### Sample JSON Inputs

```json
{
  "opportunity": {
    "description": "Software Engineer role...",
    "title": "Software Engineer"
  },
  "applicants": [
    {
      "unique_id": "abc123",
      "skills": ["Python", "ML"],
      "descriptions": "Developed an NLP model...",
      "optional": {
        "job_titles": ["Data Scientist"],
        "degrees": ["MSc CS"]
      }
    },
    {
      "unique_id": "xyz789",
      "skills": ["SQL", "Excel"],
      "descriptions": "Created dashboards...",
      "optional": {
        "job_titles": ["Business Analyst"],
        "degrees": ["MBA"]
      }
    }
  ]
}
```

### Sample JSON Outputs

```json
{
  "opportunity_title": "Software Engineer",
  "results": [
    {
      "applicant_id": "abc123",
      "similarity_score": 0.85,
      "feature_rank": 1,
      "suitability_score": 0.9
    },
    {
      "applicant_id": "xyz789",
      "similarity_score": 0.75,
      "feature_rank": 2,
      "suitability_score": 0.8
    }
  ]
}
```

### Reasoning

- **Inputs**:
  - `opportunity`: Contains the description and optionally the title of the job opportunity.
  - `applicants`: An array of objects, each holding the unique identifier, skills, and descriptions of the applicant's previous roles. They also optionally contain job titles and degrees.

- **Outputs**:
  - `opportunity_title`: To specify the job opportunity.
  - `results`: An array of objects, each containing:
    - `applicant_id`: To identify which applicant the output refers to.
    - `similarity_score`: The score generated through BERT and cosine similarity.
    - `feature_rank`: The rank based on `opportunity_id`.
    - `suitability_score`: The final score indicating the applicant's suitability for an interview.
