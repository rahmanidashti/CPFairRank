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
