# CPFairRank
Extension of CPFair

## Datasets
All the datasets used in the experiments are in the `datasets` folder. Each dataset contains several files and a folder including:

### Files
  - *ratings_data.txt*: The raw rating data file
  - *[DatasetName]_data.txt*: Interaction data after pre-processing steps
  - *[DatasetName]_inters.txt*: Interaction data from `Cornac` with Cornac ids
  - *[DatasetName]_train.txt*: Train data
  - *[DatasetName]_test.txt*: Test data
  - *[DatasetName]_tune.txt*: Validation/tune data

### Folder
  - __groups__: The *group* folder includes two sub-folders:
    - __items__: In the *items* folder we have another folder, __020__, that indicates we use top 20% of items as short-head (popular) items and the rest 80% items as long-tail (unpopular) items. Thus, it contains two files, the item groups (`longtail_items.txt` and `shorthead_items.txt`).
    - __users__: In *users* folder we have three sub-folders including `005`, `020`, and `20`. In this paper, we use `005` and `20` user grouping. `005` is the first user grouping method, __UG1__, and `20` is the second user grouping method, __UG2__. Each folder includes two user group files, i.e., `active_ids.txt` and `inactive_ids.txt`:
      
      - `005`: The level of user activity (__UG1__)
      - `20`: The consumption of popular items in user profile (__UG2__)

## Recommendation Lists (rec_lists)
The `rec_lists` folder contains all the generated recommendations for users based on the models and datassets.

- The files are tab-seprated in which the first column is a `user_id` and the second column is the list of id of recommended items (`item_ids`).
- For the unfairness-aware recommendation (`N`), we have top-50 while for fairness-aware recommendation (`C`, `P`, or `CP`) we only have the top-10 recommended items.
- The filename structure is `rec_list_[DATASET]_[BASE-MODEL]_[ReRanking-MODEL].txt`
