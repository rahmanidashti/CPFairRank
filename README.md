# CPFairRank
Extension of CPFair

## Datasets
All the datasets used in the experiments are in the `datasets` folder. Each dataset contains several files and a folder including:

### Folder
  - groups: includes two sub-folders, `items` and `users`, in the items folder we have the item groups (`longtail_items.txt` and `shorthead_items.txt`) and in users folder we have two folders (`005`,  `20`). `005` referes to the first user grouping method, UG1 and `20` is the econf user grouping method, i.e., UG2 and each includes two user group files, i.e., `active_ids.txt` and `inactive_ids.txt`.
### Files
  - ratings_data.txt
  - [DatasetName]_data.txt
  - [DatasetName]_inters.txt
  - [DatasetName]_train.txt
  - [DatasetName]_test.txt
  - [DatasetName]_tune.txt

## Recommendation Lists (rec_lists)
The `rec_lists` folder contains all the generated recommendations for users based on the models and datassets.

- The files are tab-seprated in which the first column is a `user_id` and the second column is the list of id of recommended items (`item_ids`).
- For the unfairness-aware recommendation (`N`), we have top-50 while for fairness-aware recommendation (`C`, `P`, or `CP`) we only have the top-10 recommended items.
- The filename structure is `rec_list_[DATASET]_[BASE-MODEL]_[ReRanking-MODEL].txt`
