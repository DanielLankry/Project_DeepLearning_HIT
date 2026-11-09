# Football model training

`Model_training.ipynb` downloads the configured Roboflow dataset and trains a YOLO model in Google Colab.

## Supply your own Roboflow key

The notebook reads `ROBOFLOW_API_KEY` from the runtime environment and stops with a clear error if it is missing. Use your own active key; do not put a literal key in a notebook cell or tracked configuration file.

In a Colab session, run this setup cell before the training cell. The prompt hides the value and it stays in the current runtime:

```python
import getpass
import os

os.environ["ROBOFLOW_API_KEY"] = getpass.getpass("Roboflow API key: ")
```

Do not print the environment value or save notebook outputs containing credentials. A `.env` file is ignored by Git but is not automatically loaded by this notebook.

Then run the notebook in order. The package installation, dataset download and training need network access; training can incur compute costs.
