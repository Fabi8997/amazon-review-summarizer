# amazon-review-summarizer
Repository containing the project for the course on Business and Project Management at the University of Pisa.
The goal of the project is to apply **generative ai** techniques on use cases related to business and management, in our case the aim is create a system capable of **summarizing** the many reviews referring to a single product so as to be able to give an overview of it without necessarily having to scroll through them all. This also makes it possible to have a textual correspondent to the commonly present star rating system. In this way it is possible to understand the pros and cons of the product instead of having only a general representation of the quality of the object.

We've used different models:
+ T5 (base and large)
+ BART (base, large, large-cnn, large-xsum)
+ pegasus (base, large)

Our approach consists in different iteration of summarization as follows:
1. Compute N batches;
2. Obtain for each batch a summary;
3. Clean the text, since some models add puctuation marks or words to highlight
that it’s a summmary;
4. If we’ve more reviews than a determined threshold, start again from the point
1, but now the batches are obtained starting from the summaries obtained from
the previous stage

In the report there is an explaination of the procedure and the final results obtained.
