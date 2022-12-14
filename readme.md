### Readme for NCNN
#### Prerequisites
Python 3

Pytorch 1.8.0

Pytorch-geometric

#### Data
The original data files are not provided within this codebase, as some of them require applying for access. Once you download all of them, please put them in this codebase.

##### GEO and GTEx
The GEO and GTEx data we used in our paper is a third-party data available at https://cbcl.ics.uci.edu/public_data/D-GEX/. The authors had no special access privileges, and other researchers would be able to access this data in the same manner. The data you will download is:

bgedv2_QNORM.gctx and GTEx_RNASeq_RPKM_n2921x55993.gctx.

Please put the downloaded file in the folder pre_preprocessing. 

The preprocessing is done by running:

1.gct2npy.py

2.kmeans.py

3.nodup_idx.py

4.bgedv2.py

5.bgedv2_reqnorm.py

6.bgedv2_norm.py

7.GTEx.py

8.GTEx_reqnorm.py

9.GTEx_norm.py

in order.

After preprocessing, you will have these files:

###### GEO datasets

bgedv2_X_tr_float64.npy

bgedv2_X_va_float64.npy

bgedv2_X_te_float64.npy

bgedv2_Y_tr_float64.npy

bgedv2_Y_va_float64.npy

bgedv2_Y_te_float64.npy

###### GTEx datasets

GTEx_X_tr_float64.npy

GTEx_X_va_float64.npy

GTEx_X_te_float64.npy

GTEx_Y_tr_float64.npy

GTEx_Y_va_float64.npy

GTEx_Y_te_float64.npy

Please put them in this folder.

##### Gene graph data
The gene interaction graph data can be downloaded from 

https://string-db.org/cgi/download.pl?sessionId=qJO5wpaPqJC7&species_text=Homo+sapiens.

After downloading the file'9606.protein.links.detailed.v11.5.txt', please put it in datastore folder.

The file 'Homo_sapiens.GRCh38.95.gtf' can be downloaded from :

ftp://ftp.ensembl.org/pub/release-95/gtf/homo_sapiens/Homo_sapiens.GRCh38.95.gtf.gz

Please put the downloaded file in datastore folder.

Run the python file make_map.py and myextract.py

Put the extracted gene interaction graph file stringDB1thres137.pth under NCNN folder.

#### Model
The proposed method NCNN is implemented and tested on two dataset-GEO dataset and GTEx dataset with two python files:

geo_NCNN_table.py and GTE_x_NCNN_table.py


The GCN model is implemented and tested on two dataset-GEO dataset and GTEx dataset with two python files:

geo_gcn_table.py and GTE_x_gcn_table.py
