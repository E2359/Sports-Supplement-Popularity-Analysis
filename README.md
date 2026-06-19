# Sports Supplement Popularity Analysis

## Project Overview

This project analyzes what drives the popularity of sports nutrition and bodybuilding supplements on Amazon. Since direct sales data is not available, we use the number of customer reviews as a proxy for product popularity. The goal is to understand how product features such as price, price per serving, rating, brand, and supplement category relate to consumer engagement.

We use exploratory data analysis and a baseline regression model to study patterns in supplement popularity. The project also includes a review-level dataset to better understand how customers interact with product reviews.

## Research Question

Which product attributes are associated with the popularity of sports nutrition and bodybuilding supplements on Amazon?

## Hypothesis

We expect product popularity to be related to review count, customer rating, price, and brand. Products with higher ratings and more reviews may appear more trustworthy to customers, while lower price per serving may make products more attractive within the same supplement category.

## Data

This project uses two datasets:

### 1. Product-Level Supplement Dataset

The main dataset contains Amazon sports nutrition and bodybuilding supplement products.

Important columns include:

- `product_name`: name of the supplement product
- `brand_name`: brand of the product
- `product_category`: type of supplement
- `price`: listed product price
- `price_per_serving`: cost per serving
- `overall_rating`: average product rating
- `number_of_reviews`: total number of customer reviews
- `verified_buyer_number`: number of verified buyers
- `verified_buyer_rating`: average rating from verified buyers

### 2. Review-Level Dataset

The supplementary dataset contains Amazon review information. It is used to study customer engagement patterns, such as review length and helpful votes.

## Methods

The analysis includes:

- Data cleaning and preprocessing
- Log transformation of review counts to reduce skew
- Exploratory data analysis
- Price and rating distribution analysis
- Brand and category comparison
- Review-level engagement analysis
- Linear regression modeling

The main outcome variable is:

```python
log_reviews = log(1 + number_of_reviews)
