<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="winogrande" />
  <meta itemprop="description" content="The  WinoGrande, a large-scale dataset of 44k problems, inspired by the original&#10; Winograd Schema Challenge design, but adjusted to improve both the scale and&#10; the hardness of the dataset.&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;winogrande&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/winogrande" />
  <meta itemprop="sameAs" content="http://winogrande.allenai.org/" />
  <meta itemprop="citation" content="@article{sakaguchi2019winogrande,&#10;    title={WinoGrande: An Adversarial Winograd Schema Challenge at Scale},&#10;    author={Sakaguchi, Keisuke and Bras, Ronan Le and Bhagavatula, Chandra and Choi, Yejin},&#10;    journal={arXiv preprint arXiv:1907.10641},&#10;    year={2019}&#10;}" />
</div>

# `winogrande`


Note: This dataset has been updated since the last stable release. The new
versions and config marked with
<span class="material-icons" title="Available only in the tfds-nightly package">nights_stay</span>
are only available in the `tfds-nightly` package.

*   **Description**:

The WinoGrande, a large-scale dataset of 44k problems, inspired by the original
Winograd Schema Challenge design, but adjusted to improve both the scale and the
hardness of the dataset.

*   **Additional Documentation**:
    <a class="button button-with-icon" href="https://paperswithcode.com/dataset/winogrande">
    Explore on Papers With Code
    <span class="material-icons icon-after" aria-hidden="true"> north_east
    </span> </a>

*   **Homepage**:
    [http://winogrande.allenai.org/](http://winogrande.allenai.org/)

*   **Source code**:
    [`tfds.text.Winogrande`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/text/winogrande.py)

*   **Versions**:

    *   **`1.2.0`** (default)
        <span class="material-icons" title="Available only in the tfds-nightly package">nights_stay</span>:
        Updated source file with more data and new checksums.

*   **Download size**: `Unknown size`

*   **Dataset size**: `Unknown size`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Unknown

*   **Splits**:

Split | Examples
:---- | -------:

*   **Feature structure**:

```python
FeaturesDict({
    'label': ClassLabel(shape=(), dtype=int64, num_classes=2),
    'option1': Text(shape=(), dtype=string),
    'option2': Text(shape=(), dtype=string),
    'sentence': Text(shape=(), dtype=string),
})
```

*   **Feature documentation**:

Feature  | Class        | Shape | Dtype  | Description
:------- | :----------- | :---- | :----- | :----------
         | FeaturesDict |       |        |
label    | ClassLabel   |       | int64  |
option1  | Text         |       | string |
option2  | Text         |       | string |
sentence | Text         |       | string |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `None`

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):
    Not supported.

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):
    Missing.

*   **Citation**:

```
@article{sakaguchi2019winogrande,
    title={WinoGrande: An Adversarial Winograd Schema Challenge at Scale},
    author={Sakaguchi, Keisuke and Bras, Ronan Le and Bhagavatula, Chandra and Choi, Yejin},
    journal={arXiv preprint arXiv:1907.10641},
    year={2019}
}
```

