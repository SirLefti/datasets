<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="ai2_arc_with_ir" />
  <meta itemprop="description" content="A new dataset of 7,787 genuine grade-school level, multiple-choice science&#10;questions, assembled to encourage research in advanced question-answering. The&#10;dataset is partitioned into a Challenge Set and an Easy Set, where the former&#10;contains only questions answered incorrectly by both a retrieval-based algorithm&#10;and a word co-occurrence algorithm. We are also including a corpus of over 14&#10;million science sentences relevant to the task, and an implementation of three&#10;neural baseline models for this dataset. We pose ARC as a challenge to the&#10;community.&#10;&#10;Compared to the original dataset, this adds context sentences obtained through&#10;information retrieval in the same way as UnifiedQA (see:&#10;https://arxiv.org/abs/2005.00700 ).&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;ai2_arc_with_ir&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/ai2_arc_with_ir" />
  <meta itemprop="sameAs" content="https://allenai.org/data/arc" />
  <meta itemprop="citation" content="@article{allenai:arc,&#10;      author    = {Peter Clark  and Isaac Cowhey and Oren Etzioni and Tushar Khot and&#10;                    Ashish Sabharwal and Carissa Schoenick and Oyvind Tafjord},&#10;      title     = {Think you have Solved Question Answering? Try ARC, the AI2 Reasoning Challenge},&#10;      journal   = {arXiv:1803.05457v1},&#10;      year      = {2018},&#10;}&#10;@article{2020unifiedqa,&#10;    title={UnifiedQA: Crossing Format Boundaries With a Single QA System},&#10;    author={D. Khashabi and S. Min and T. Khot and A. Sabhwaral and O. Tafjord and P. Clark and H. Hajishirzi},&#10;    journal={arXiv preprint},&#10;    year={2020}&#10;}" />
</div>

# `ai2_arc_with_ir`


*   **Description**:

A new dataset of 7,787 genuine grade-school level, multiple-choice science
questions, assembled to encourage research in advanced question-answering. The
dataset is partitioned into a Challenge Set and an Easy Set, where the former
contains only questions answered incorrectly by both a retrieval-based algorithm
and a word co-occurrence algorithm. We are also including a corpus of over 14
million science sentences relevant to the task, and an implementation of three
neural baseline models for this dataset. We pose ARC as a challenge to the
community.

Compared to the original dataset, this adds context sentences obtained through
information retrieval in the same way as UnifiedQA (see:
https://arxiv.org/abs/2005.00700 ).

*   **Homepage**: [https://allenai.org/data/arc](https://allenai.org/data/arc)

*   **Source code**:
    [`tfds.datasets.ai2_arc_with_ir.Builder`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/datasets/ai2_arc_with_ir/ai2_arc_with_ir_dataset_builder.py)

*   **Versions**:

    *   **`1.0.0`** (default): No release notes.

*   **Download size**: `3.68 MiB`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Yes

*   **Feature structure**:

```python
FeaturesDict({
    'answerKey': ClassLabel(shape=(), dtype=int64, num_classes=5),
    'choices': Sequence({
        'label': ClassLabel(shape=(), dtype=int64, num_classes=5),
        'text': Text(shape=(), dtype=string),
    }),
    'id': Text(shape=(), dtype=string),
    'paragraph': Text(shape=(), dtype=string),
    'question': Text(shape=(), dtype=string),
})
```

*   **Feature documentation**:

Feature       | Class        | Shape | Dtype  | Description
:------------ | :----------- | :---- | :----- | :----------
              | FeaturesDict |       |        |
answerKey     | ClassLabel   |       | int64  |
choices       | Sequence     |       |        |
choices/label | ClassLabel   |       | int64  |
choices/text  | Text         |       | string |
id            | Text         |       | string |
paragraph     | Text         |       | string |
question      | Text         |       | string |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `None`

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):
    Not supported.

*   **Citation**:

```
@article{allenai:arc,
      author    = {Peter Clark  and Isaac Cowhey and Oren Etzioni and Tushar Khot and
                    Ashish Sabharwal and Carissa Schoenick and Oyvind Tafjord},
      title     = {Think you have Solved Question Answering? Try ARC, the AI2 Reasoning Challenge},
      journal   = {arXiv:1803.05457v1},
      year      = {2018},
}
@article{2020unifiedqa,
    title={UnifiedQA: Crossing Format Boundaries With a Single QA System},
    author={D. Khashabi and S. Min and T. Khot and A. Sabhwaral and O. Tafjord and P. Clark and H. Hajishirzi},
    journal={arXiv preprint},
    year={2020}
}
```


## ai2_arc_with_ir/ARC-Challenge-IR (default config)

*   **Config description**: Challenge Set of 2590 "hard" questions (those that
    both a retrieval and a co-occurrence method fail to answer correctly)

*   **Dataset size**: `3.76 MiB`

*   **Splits**:

Split          | Examples
:------------- | -------:
`'test'`       | 1,172
`'train'`      | 1,119
`'validation'` | 299

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):

<!-- mdformat off(HTML should not be auto-formatted) -->

{% framebox %}

<button id="displaydataframe">Display examples...</button>
<div id="dataframecontent" style="overflow-x:auto"></div>
<script>
const url = "https://storage.googleapis.com/tfds-data/visualization/dataframe/ai2_arc_with_ir-ARC-Challenge-IR-1.0.0.html";
const dataButton = document.getElementById('displaydataframe');
dataButton.addEventListener('click', async () => {
  // Disable the button after clicking (dataframe loaded only once).
  dataButton.disabled = true;

  const contentPane = document.getElementById('dataframecontent');
  try {
    const response = await fetch(url);
    // Error response codes don't throw an error, so force an error to show
    // the error message.
    if (!response.ok) throw Error(response.statusText);

    const data = await response.text();
    contentPane.innerHTML = data;
  } catch (e) {
    contentPane.innerHTML =
        'Error loading examples. If the error persist, please open '
        + 'a new issue.';
  }
});
</script>

{% endframebox %}

<!-- mdformat on -->

## ai2_arc_with_ir/ARC-Easy-IR

*   **Config description**: Easy Set of 5197 questions for the ARC Challenge.

*   **Dataset size**: `7.49 MiB`

*   **Splits**:

Split          | Examples
:------------- | -------:
`'test'`       | 2,376
`'train'`      | 2,251
`'validation'` | 570

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):

<!-- mdformat off(HTML should not be auto-formatted) -->

{% framebox %}

<button id="displaydataframe">Display examples...</button>
<div id="dataframecontent" style="overflow-x:auto"></div>
<script>
const url = "https://storage.googleapis.com/tfds-data/visualization/dataframe/ai2_arc_with_ir-ARC-Easy-IR-1.0.0.html";
const dataButton = document.getElementById('displaydataframe');
dataButton.addEventListener('click', async () => {
  // Disable the button after clicking (dataframe loaded only once).
  dataButton.disabled = true;

  const contentPane = document.getElementById('dataframecontent');
  try {
    const response = await fetch(url);
    // Error response codes don't throw an error, so force an error to show
    // the error message.
    if (!response.ok) throw Error(response.statusText);

    const data = await response.text();
    contentPane.innerHTML = data;
  } catch (e) {
    contentPane.innerHTML =
        'Error loading examples. If the error persist, please open '
        + 'a new issue.';
  }
});
</script>

{% endframebox %}

<!-- mdformat on -->