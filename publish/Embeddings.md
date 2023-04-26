---
title:  "Embeddings"
created: Sunday 23rd April 2023 08:52
excerpt: "An embedding is a numerical representation of data objects, such as words, phrases, or even entire document, in a Continuous Vector Space. They are used to capture semantic meaning, relationships, and other properties of the original data in a format that is more suitable for machine learning algorithms."
---

### What is an embedding?
An [embedding](https://platform.openai.com/docs/guides/embeddings/what-are-embeddings), in the context of artificial intelligence (AI) and particularly in natural language processing (NLP) and machine learning, is a numerical representation of data objects, such as words, phrases, or even entire documents, in a [[continuous-vector-space|Continuous Vector Space]]. Embeddings are used to capture the semantic meaning, relationships, and other properties of the original data in a lower-dimensional, dense, and continuous format, making them more suitable for machine learning algorithms.

### What is the goal of an embedding?
The main goal of creating embeddings is to transform discrete and sparse data (like text) into a continuous and dense representation that preserves semantic information while being more efficient to process. This conversion helps improve the performance of various NLP and machine learning tasks, such as text classification, sentiment analysis, machine translation, and recommendation systems.

### How can I create an embedding?
You can use the [OpenAI embeddings API](https://platform.openai.com/docs/api-reference/embeddings/create?lang=node.js)

```js
const res = await fetch("https://api.openai.com/v1/embeddings", {
	headers: {
		"Content-Type": "application/json",
		Authorization: `Bearer ${apiKey}`
	},
	method: "POST",
	body: JSON.stringify({
		model: "text-embedding-ada-002",
		input
	})
});

const json = await res.json();
const embedding = json.data[0].embedding;
```

### What are some use cases for embeddings?
From OpenAI documentation:
-   **Search** (where results are ranked by relevance to a query string)
-   **Clustering** (where text strings are grouped by similarity)
-   **Recommendations** (where items with related text strings are recommended)
-   **Anomaly detection** (where outliers with little relatedness are identified)
-   **Diversity measurement** (where similarity distributions are analyzed)
-   **Classification** (where text strings are classified by their most similar label)
