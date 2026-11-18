# Boardroom pitch script (target 5-7 minutes, about 40 s per slide)

## Slide 1: HarborCart: Who are our customers and what should we do?
Good day. We are VoltesFive. HarborCart is a fictional Philippine marketplace. We used a public UK retail dataset as a stand-in to show how customer data can guide marketing and retention decisions. All findings describe that dataset.

## Slide 2: The business problem
Without segments, every customer gets the same message. We asked three questions: how do customers differ, which groups matter most, and what should HarborCart do for each.

## Slide 3: Our approach: CRISP-DM end to end
Data preparation followed the audit trail in our report. We logged every experiment, chose the number of clusters with a rule fixed in advance, and avoided leakage in the prediction task by building features only from before the cutoff date.

## Slide 4: A few customers drive most of the sales
Sales are concentrated. The top twenty percent of customers account for 75% of recorded sales. This is why protecting high-value customers is a priority.

## Slide 5: 3 customer segments
k-Means on log-scaled RFM gave 3 groups. The biggest revenue segment, Loyal High-Value, is 18% of customers but 68% of sales. Cluster quality is moderate by silhouette, so we treat segments as useful guides, not hard boundaries.

## Slide 6: What each segment looks like
This heatmap shows how each group behaves. Recency is days since last purchase, so lower is better. Names such as Lapsed or Loyal are labels we assigned from the medians.

## Slide 7: Products bought together
Market-basket analysis found 1215 strong product pairs. The strongest has lift 18.6, meaning the items appear together that many times more often than chance. These are ideas for bundles and cross-sell, not proof of cause.

## Slide 8: Predicting repeat purchases
We predict whether a customer buys again in the final ninety days. On a held-out test set the model reaches an AUC of 0.73, compared with 0.50 for guessing. The most influential feature is Frequency.

## Slide 9: Recommendations and next steps
Each segment gets a different goal. Benefits are unverified, so we recommend small A/B tests first. Limits: the data is a UK retailer from 2010 to 2011, so real HarborCart data must be used before any decision. Thank you.

