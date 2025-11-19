# TimeLine Summarization

## Dataset

CNTLS is our constructed new TimeLine Summarization dataset for Chinese News. It has 77 topics and timelines. You can download the Dataset from google drive (https://drive.google.com/drive/u/1/folders/1a_Q3jAI5jqiSlBx1r8m01rjATsvPtY6Z), and you can also download the raw data from here. 
Please refer Mao, Q., Wang, J., Wang, Z., Li, X., Li, B., & Li, J. (2021). CNTLS: A Benchmark Dataset for Abstractive or Extractive Chinese Timeline Summarization. arXiv preprint arXiv:2105.14201.

CNTLS-Fin is in the folder "datasets/chinese-example", which is our constructed financial timeline dataset.

## Library installation
To install requirements, run:
```
pip install -r requirements.txt
pip install -e .
```
[Tilse](https://github.com/smartschat/tilse) also needs to be installed for evaluation and some TLS-specific data classes.

## Run 

```
python evaluate.py  \
  --dataset datasets/CNTLS-Fin/ \
  --method datewise \
  --output test15/tlcn.datewise-lk.json \
  --language chinese \
  --summarizer centriodrank \
  --date_select regression\
  --resources resources/datewise \
  --mode eval \
  --l \
  --k
```


