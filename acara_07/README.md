# BIC30007-2 - Acara 7
See the main [README.md](../README.md) for general instructions.

## Using Google Colaboratory
### Upload the repository to Google Drive
The best way to run this course repository on google colab is via Google Drive.

If you haven't so:
- Find the latest release from: https://github.com/lab-biotek-bio-ugm/BIC30007-2/releases
- Go to the `Assets` and download the source code (either `zip` or `tar.gz`)
- Unzip (or untar) the source code in your local machine (laptop)
- Upload the whole directory to Google drive
- Open the notebook with google colab

### Installing dependencies
- On the first line, create a new cell and run:

```python
# install conda and mamba
!pip install -q condacolab
import condacolab
condacolab.install_mambaforge() # session will crash and restart
```
- Setelah session restart
```python
import condacolab
condacolab.check()

# mount drive
from google.colab import drive
drive.mount('/content/drive')
```
- Install dependencies
```python
# assume you have uploaded the repo to gdrive
!mamba env update -n base -f /content/drive/MyDrive/<your downloaded release name>/acara_07/environment.yml
```