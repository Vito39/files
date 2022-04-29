# Welcome to Polly Python3 Notebook.
*[jump to query_metadata](#query_metadata)<br>
*[jump to get_all_omixatlas](#get_all_omixatlas)<br>
*[jump to omixatlas_summary](#omixatlas_summary)<br>
*[jump to get_schema](#get_schema)<br>
*[jump to insert_schema](#insert_schema)<br>
*[jump to update](#update_schema)<br>

### to install polly python on jupyter notebook


```python
!sudo pip3 install polly-python --quiet 
```

    [33mWARNING: You are using pip version 19.2.3, however version 21.3.1 is available.
    You should consider upgrading via the 'pip install --upgrade pip' command.[0m


### importing modules


```python
from polly.auth import Polly
from polly.omixatlas import OmixAtlas
```

### authentication


```python
import os
AUTH_TOKEN=os.environ['POLLY_REFRESH_TOKEN'] 
polly = Polly()                              
polly.auth(AUTH_TOKEN)
```

### making object to use class functions


```python
omixatlas = OmixAtlas() 
```

### get_all_omixatlas
### input 
None
### output
it will return a list of obejcts which contains the information about
<a id="get_all_omixatlas"></a>


```python
omixatlas.get_all_omixatlas()
```




    {'data': [{'repo_name': 'atavistik',
       'repo_id': '1650348922627',
       'indexes': {'gct_metadata': 'atavistik_gct_metadata',
        'h5ad_metadata': 'atavistik_h5ad_metadata',
        'csv': 'atavistik_csv',
        'files': 'atavistik_files',
        'json': 'atavistik_json',
        'ipynb': 'atavistik_ipynb',
        'gct_data': 'atavistik_gct_data',
        'h5ad_data': 'atavistik_h5ad_data'},
       'diseases': ['none'],
       'organisms': ['none'],
       'sources': ['none'],
       'datatypes': [],
       'dataset_count': 1,
       'disease_count': 1,
       'tissue_count': 1,
       'organism_count': 1,
       'cell_line_count': 0,
       'cell_type_count': 0,
       'drug_count': 0,
       'data_type_count': 0,
       'data_source_count': 1,
       'sample_count': 0,
       'normal_sample_count': 0},
      {'repo_name': 'gdx',
       'repo_id': '1646370413059',
       'indexes': {'gct_metadata': 'gdx_gct_metadata',
        'h5ad_metadata': 'gdx_h5ad_metadata',
        'csv': 'gdx_csv',
        'files': 'gdx_files',
        'json': 'gdx_json',
        'ipynb': 'gdx_ipynb',
        'gct_data': 'gdx_gct_data',
        'h5ad_data': 'gdx_h5ad_data'},
       'diseases': [],
       'organisms': [],
       'sources': [],
       'datatypes': [],
       'dataset_count': 0,
       'disease_count': 0,
       'tissue_count': 0,
       'organism_count': 0,
       'cell_line_count': 0,
       'cell_type_count': 0,
       'drug_count': 0,
       'data_type_count': 0,
       'data_source_count': 0,
       'sample_count': 0,
       'normal_sample_count': 0},
      {'repo_name': 'auron_data_lake',
       'repo_id': '1613041985263',
       'indexes': {'gct_metadata': 'auron_data_lake_gct_metadata',
        'h5ad_metadata': 'auron_data_lake_h5ad_metadata',
        'csv': 'auron_data_lake_csv',
        'files': 'auron_data_lake_files',
        'json': 'auron_data_lake_json',
        'ipynb': 'auron_data_lake_ipynb',
        'gct_data': 'auron_data_lake_gct_data',
        'h5ad_data': 'auron_data_lake_h5ad_data'},
       'diseases': ['small cell lung carcinoma',
        'carcinoma, small cell',
        'carcinoma, neuroendocrine',
        'normal',
        '[normal]',
        'neuroendocrine tumors',
        'carcinoma, hepatocellular',
        'carcinoma, non-small-cell lung',
        'leukemia, myeloid, acute',
        'neoplasm metastasis',
        'neoplasms, squamous cell',
        'prostatic neoplasms',
        'urinary bladder neoplasms',
        '[aml]',
        '[leukemia, acute myeloid, neuroblastoma]',
        '[leukemia, acute myeloid, normal]',
        '[leukemia, acute myeloid]',
        '[neuroblastoma, skin cancer]',
        'adenocarcinoma of lung',
        'adenoma, chromophobe'],
       'organisms': ['homo sapiens', 'mus musculus', '[homo sapiens]'],
       'sources': ['geo', 'auron', 'pubmed', 'tcga'],
       'datatypes': ['raw counts transcriptomics', 'transcriptomics'],
       'dataset_count': 33,
       'disease_count': 53,
       'tissue_count': 68,
       'organism_count': 3,
       'cell_line_count': 22,
       'cell_type_count': 32,
       'drug_count': 503,
       'data_type_count': 2,
       'data_source_count': 4,
       'sample_count': 12457,
       'normal_sample_count': 1416},
      {'repo_name': 'hpa',
       'repo_id': '1619514006627',
       'indexes': {'gct_metadata': 'hpa_gct_metadata',
        'h5ad_metadata': 'hpa_h5ad_metadata',
        'csv': 'hpa_csv',
        'files': 'hpa_files',
        'json': 'hpa_json',
        'ipynb': 'hpa_ipynb',
        'gct_data': 'hpa_gct_data',
        'h5ad_data': 'hpa_h5ad_data'},
       'diseases': ['normal'],
       'organisms': ['homo sapiens', 'sus (pig)', 'mus musculus'],
       'sources': ['hpa'],
       'datatypes': ['transcriptomics', 'gene expression reliability'],
       'dataset_count': 1755,
       'disease_count': 1,
       'tissue_count': 78,
       'organism_count': 3,
       'cell_line_count': 70,
       'cell_type_count': 150,
       'drug_count': 1,
       'data_type_count': 2,
       'data_source_count': 1,
       'sample_count': 678,
       'normal_sample_count': 678},
      {'repo_name': 'teddy',
       'repo_id': '1615464367934',
       'indexes': {'gct_metadata': 'teddy_gct_metadata',
        'h5ad_metadata': 'teddy_h5ad_metadata',
        'csv': 'teddy_csv',
        'files': 'teddy_files',
        'json': 'teddy_json',
        'ipynb': 'teddy_ipynb',
        'gct_data': 'teddy_gct_data',
        'h5ad_data': 'teddy_h5ad_data'},
       'diseases': ['none', 'diabetes mellitus, type 1'],
       'organisms': ['homo sapiens'],
       'sources': ['metabolomics workbench'],
       'datatypes': ['lipidomics', 'metabolomics'],
       'dataset_count': 34518,
       'disease_count': 2,
       'tissue_count': 1,
       'organism_count': 1,
       'cell_line_count': 1,
       'cell_type_count': 1,
       'drug_count': 1,
       'data_type_count': 2,
       'data_source_count': 1,
       'sample_count': 11565,
       'normal_sample_count': 0},
      {'repo_name': 'valo_onco',
       'repo_id': '1649184014614',
       'indexes': {'gct_metadata': 'valo_onco_gct_metadata',
        'h5ad_metadata': 'valo_onco_h5ad_metadata',
        'csv': 'valo_onco_csv',
        'files': 'valo_onco_files',
        'json': 'valo_onco_json',
        'ipynb': 'valo_onco_ipynb',
        'gct_data': 'valo_onco_gct_data',
        'h5ad_data': 'valo_onco_h5ad_data'},
       'diseases': ['normal',
        'breast neoplasms',
        'neoplasms',
        'brain neoplasms',
        'carcinoma, non-small-cell lung',
        'colonic neoplasm',
        'kidney neoplasms',
        'leukemia',
        'melanoma',
        'ovarian neoplasms',
        'prostatic neoplasms',
        'stomach neoplasm',
        'central nervous system neoplasms',
        'hematologic neoplasms',
        'leukemia, myeloid, acute',
        'leukemia, t-cell',
        'multiple myeloma',
        'neoplasms, squamous cell',
        'precursor t-cell lymphoblastic leukemia-lymphoma',
        'zika virus infection'],
       'organisms': ['homo sapiens', 'mus musculus'],
       'sources': ['geo'],
       'datatypes': ['transcriptomics', 'raw counts transcriptomics'],
       'dataset_count': 19,
       'disease_count': 20,
       'tissue_count': 14,
       'organism_count': 2,
       'cell_line_count': 28,
       'cell_type_count': 17,
       'drug_count': 3,
       'data_type_count': 2,
       'data_source_count': 1,
       'sample_count': 202,
       'normal_sample_count': 32},
      {'repo_name': 'gdc',
       'repo_id': '1623221686703',
       'indexes': {'gct_metadata': 'gdc_gct_metadata',
        'h5ad_metadata': 'gdc_h5ad_metadata',
        'csv': 'gdc_csv',
        'files': 'gdc_files',
        'json': 'gdc_json',
        'ipynb': 'gdc_ipynb',
        'gct_data': 'gdc_gct_data',
        'h5ad_data': 'gdc_h5ad_data'},
       'diseases': ['leukemia, myeloid, acute',
        'precursor t-cell lymphoblastic leukemia-lymphoma',
        'multiple myeloma',
        'precursor b-cell lymphoblastic leukemia-lymphoma',
        'lymphoma, large b-cell, diffuse',
        'wilms tumor',
        'burkitt lymphoma, nos (includes all variants)',
        'squamous cell carcinoma, nonkeratinizing, nos',
        'rhabdoid tumor',
        'adenocarcinoma, nos',
        'squamous cell carcinoma, keratinizing, nos',
        'none',
        'neuroblastoma',
        'infiltrating duct carcinoma, nos',
        'adenocarcinoma, metastatic, nos',
        'myelodysplastic syndromes',
        'osteosarcoma, nos',
        'not reported',
        'unknown',
        'leukemia, biphenotypic, acute'],
       'organisms': ['homo sapiens'],
       'sources': ['gdc'],
       'datatypes': ['mirna expression',
        'transcriptomics',
        'copy number variation'],
       'dataset_count': 9908,
       'disease_count': 67,
       'tissue_count': 41,
       'organism_count': 1,
       'cell_line_count': 1,
       'cell_type_count': 1,
       'drug_count': 1,
       'data_type_count': 3,
       'data_source_count': 1,
       'sample_count': 5353,
       'normal_sample_count': 0},
      {'repo_name': 'geo',
       'repo_id': '9',
       'indexes': {'gct_metadata': 'geo_gct_metadata',
        'h5ad_metadata': 'geo_h5ad_metadata',
        'csv': 'geo_csv',
        'files': 'geo_files',
        'ipynb': 'geo_ipynb',
        'gct_data': 'geo_gct_data',
        'h5ad_data': 'geo_h5ad_data'},
       'diseases': ['normal',
        'neoplasms',
        'breast neoplasms',
        'obesity',
        'carcinoma, hepatocellular',
        'prostatic neoplasms',
        'melanoma',
        'leukemia, myeloid, acute',
        'colorectal neoplasms',
        'glioblastoma',
        'colonic neoplasms',
        'diabetes mellitus',
        'diabetes mellitus, type 2',
        'adenocarcinoma of lung',
        'triple negative breast neoplasms',
        'ovarian neoplasms',
        'leukemia',
        'autoimmune diseases',
        'neuroblastoma',
        'neoplasm metastasis'],
       'organisms': ['homo sapiens',
        'mus musculus',
        'rattus norvegicus',
        'caenorhabditis elegans',
        'escherichia coli',
        'arabidopsis thaliana',
        'danio rerio',
        'saccharomyces cerevisiae',
        'macaca mulatta',
        'macaca fascicularis',
        'pan troglodytes',
        'gallus gallus',
        'homo sapiens,mus musculus',
        'chlorocebus aethiops',
        'chlorocebus sabaeus',
        'mesocricetus auratus',
        'papio hamadryas',
        'bos taurus',
        'microcebus murinus',
        'rattus rattus'],
       'sources': ['geo'],
       'datatypes': ['transcriptomics',
        'single cell',
        'raw counts transcriptomics',
        'snp array'],
       'dataset_count': 63532,
       'disease_count': 3374,
       'tissue_count': 1004,
       'organism_count': 108,
       'cell_line_count': 5245,
       'cell_type_count': 791,
       'drug_count': 1598,
       'data_type_count': 4,
       'data_source_count': 1,
       'sample_count': 1556378,
       'normal_sample_count': 1017118},
      {'repo_name': 'rcsb_structures',
       'repo_id': '1639402777465',
       'indexes': {'gct_metadata': 'rcsb_structures_gct_metadata',
        'h5ad_metadata': 'rcsb_structures_h5ad_metadata',
        'csv': 'rcsb_structures_csv',
        'files': 'rcsb_structures_files',
        'json': 'rcsb_structures_json',
        'ipynb': 'rcsb_structures_ipynb',
        'gct_data': 'rcsb_structures_gct_data',
        'h5ad_data': 'rcsb_structures_h5ad_data'},
       'diseases': ['normal'],
       'organisms': ['homo sapiens',
        'none',
        'escherichia coli',
        'mus musculus',
        'rattus norvegicus',
        'saccharomyces cerevisiae',
        'mycobacterium tuberculosis',
        'pseudomonas aeruginosa',
        'arabidopsis thaliana',
        'staphylococcus aureus',
        'severe acute respiratory syndrome coronavirus 2',
        'bos taurus',
        'human immunodeficiency virus 1',
        'bacillus subtilis',
        'synthetic construct',
        'thermus thermophilus',
        'gallus gallus',
        'drosophila melanogaster',
        'enterobacteria phage t4',
        'escherichia coli (strain k12)'],
       'sources': ['rcsb'],
       'datatypes': ['structural biology'],
       'dataset_count': 135144,
       'disease_count': 1,
       'tissue_count': 186,
       'organism_count': 6852,
       'cell_line_count': 165,
       'cell_type_count': 145,
       'drug_count': 1,
       'data_type_count': 1,
       'data_source_count': 1,
       'sample_count': 0,
       'normal_sample_count': 0},
      {'repo_name': 'auron_single_cell_atlas',
       'repo_id': '1649415790935',
       'indexes': {'gct_metadata': 'auron_single_cell_atlas_gct_metadata',
        'h5ad_metadata': 'auron_single_cell_atlas_h5ad_metadata',
        'csv': 'auron_single_cell_atlas_csv',
        'files': 'auron_single_cell_atlas_files',
        'json': 'auron_single_cell_atlas_json',
        'ipynb': 'auron_single_cell_atlas_ipynb',
        'gct_data': 'auron_single_cell_atlas_gct_data',
        'h5ad_data': 'auron_single_cell_atlas_h5ad_data'},
       'diseases': [],
       'organisms': [],
       'sources': [],
       'datatypes': [],
       'dataset_count': 0,
       'disease_count': 0,
       'tissue_count': 0,
       'organism_count': 0,
       'cell_line_count': 0,
       'cell_type_count': 0,
       'drug_count': 0,
       'data_type_count': 0,
       'data_source_count': 0,
       'sample_count': 0,
       'normal_sample_count': 0},
      {'repo_name': 'transcriptomics__celt',
       'repo_id': '1612862312240',
       'indexes': {'gct_metadata': 'transcriptomics__celt_gct_metadata',
        'h5ad_metadata': 'transcriptomics__celt_h5ad_metadata',
        'csv': 'transcriptomics__celt_csv',
        'files': 'transcriptomics__celt_files',
        'json': 'transcriptomics__celt_json',
        'ipynb': 'transcriptomics__celt_ipynb',
        'gct_data': 'transcriptomics__celt_gct_data',
        'h5ad_data': 'transcriptomics__celt_h5ad_data'},
       'diseases': ['crohn disease',
        'ulcerative colitis',
        'colorectal cancer',
        'enteric nervous system',
        'non-small-cell lung cancer',
        'melanoma',
        'pediatric obesity',
        'carcinoma, hepatocellular',
        'inflammatory bowel disease',
        'pediatric crohn disease',
        'urinary bladder neoplasms',
        'breast cancer',
        'prostatic neoplasms',
        'uveal melanoma',
        'carcinoma, ductal',
        'cholangiocarcinoma',
        'head and neck squamous cell carcinomas',
        'non-alcoholic fatty liver disease',
        'normal',
        'pancreatic neoplasms'],
       'organisms': ['homo sapiens', 'mus musculus'],
       'sources': ['gene expression omnibus (geo)', 'geo', 'publication'],
       'datatypes': ['single cell', 'transcriptomics'],
       'dataset_count': 92,
       'disease_count': 48,
       'tissue_count': 36,
       'organism_count': 2,
       'cell_line_count': 4,
       'cell_type_count': 37,
       'drug_count': 4,
       'data_type_count': 2,
       'data_source_count': 3,
       'sample_count': 4718,
       'normal_sample_count': 0},
      {'repo_name': 'enterprise_atlas',
       'repo_id': '1638441282192',
       'indexes': {'gct_metadata': 'enterprise_atlas_gct_metadata',
        'h5ad_metadata': 'enterprise_atlas_h5ad_metadata',
        'csv': 'enterprise_atlas_csv',
        'files': 'enterprise_atlas_files',
        'json': 'enterprise_atlas_json',
        'ipynb': 'enterprise_atlas_ipynb',
        'gct_data': 'enterprise_atlas_gct_data',
        'h5ad_data': 'enterprise_atlas_h5ad_data'},
       'diseases': ['breast neoplasms',
        'endometrial neoplasms',
        'endometriosis',
        'none',
        'triple negative breast neoplasms',
        'smith-magenis',
        'tay–sachs',
        'carcinoma, hepatocellular',
        'infertility',
        'neoplasm metastasis',
        'neoplasms, basal cell',
        'carcinoma',
        'hereditary breast and ovarian cancer syndrome',
        'influenza, human',
        'leiomyoma',
        'neuroblastoma',
        'normal',
        'prostatic neoplasms',
        'autoimmune diseases',
        'bone marrow neoplasms'],
       'organisms': ['homo sapiens', 'mus musculus'],
       'sources': ['geo', 'proprietary'],
       'datatypes': ['transcriptomics', 'single cell', 'mutation', 'mirna'],
       'dataset_count': 173,
       'disease_count': 36,
       'tissue_count': 25,
       'organism_count': 2,
       'cell_line_count': 96,
       'cell_type_count': 44,
       'drug_count': 22,
       'data_type_count': 4,
       'data_source_count': 2,
       'sample_count': 8962,
       'normal_sample_count': 3939},
      {'repo_name': 'cptac',
       'repo_id': '1609924165364',
       'indexes': {'gct_metadata': 'cptac_gct_metadata',
        'h5ad_metadata': 'cptac_h5ad_metadata',
        'csv': 'cptac_csv',
        'files': 'cptac_files',
        'json': 'cptac_json',
        'ipynb': 'cptac_ipynb',
        'gct_data': 'cptac_gct_data',
        'h5ad_data': 'cptac_h5ad_data'},
       'diseases': ['carcinoma, hepatocellular',
        'glucose-galactose malabsorption',
        'squamous cell carcinoma of head and neck',
        'hereditary leiomyomatosis and renal cell cancer',
        'uterine endometrial carcinoma',
        'colonic neoplasms',
        'breast cancer',
        'ovarian neoplasms',
        'adenocarcinoma',
        'brain neoplasms',
        'breast neoplasms',
        'carcinoma',
        'glioblastoma'],
       'organisms': ['homo sapiens'],
       'sources': ['cptac'],
       'datatypes': ['proteomics',
        'phosphoproteomics',
        'transcriptomics',
        'copy number variation',
        'mutation',
        'mirna expression',
        'acetylproteomics',
        'methylation',
        'lipidomics',
        'metabolomics'],
       'dataset_count': 6542,
       'disease_count': 13,
       'tissue_count': 33,
       'organism_count': 1,
       'cell_line_count': 1,
       'cell_type_count': 1,
       'drug_count': 1,
       'data_type_count': 10,
       'data_source_count': 1,
       'sample_count': 2440,
       'normal_sample_count': 0},
      {'repo_name': 'liveromix_atlas',
       'repo_id': '1615965444377',
       'indexes': {'gct_metadata': 'liveromix_atlas_gct_metadata',
        'h5ad_metadata': 'liveromix_atlas_h5ad_metadata',
        'csv': 'liveromix_atlas_csv',
        'files': 'liveromix_atlas_files',
        'json': 'liveromix_atlas_json',
        'ipynb': 'liveromix_atlas_ipynb',
        'gct_data': 'liveromix_atlas_gct_data',
        'h5ad_data': 'liveromix_atlas_h5ad_data'},
       'diseases': ['normal',
        'carcinoma, hepatocellular',
        'obesity',
        'neoplasms',
        'fatty liver',
        'non-alcoholic fatty liver disease',
        'chemical and drug induced liver injury',
        'insulin resistance',
        'diabetes mellitus',
        'diabetes mellitus, type 2',
        'coronaviridae infections',
        'metabolic syndrome',
        'hepatitis c',
        'liver neoplasms',
        'breast neoplasms',
        'colorectal neoplasms',
        'metabolic diseases',
        'glucose intolerance',
        'liver diseases',
        'hepatitis b'],
       'organisms': ['homo sapiens',
        'mus musculus',
        'rattus norvegicus',
        'danio rerio',
        'sus scrofa domesticus',
        'macaca mulatta',
        'dicentrarchus labrax',
        'mus spretus',
        'oncorhynchus mykiss',
        'marmota monax',
        'pan troglodytes',
        'capra hircus',
        'chlorocebus aethiops',
        'macaca fascicularis',
        'mus musculus domesticus',
        'arvicanthis niloticus',
        'cebus capucinus',
        'neotoma lepida',
        'papio cynocephalus',
        'papio hamadryas'],
       'sources': ['geo',
        'lincs',
        'tcga',
        'metabolomics workbench',
        'metabolights',
        'ccle',
        'cptac',
        'depmap',
        'hpa',
        'gtex'],
       'datatypes': ['transcriptomics',
        'mutation',
        'metabolomics',
        'single cell',
        'proteomics',
        'lipidomics',
        'mirna',
        'drug screens',
        'gene dependency',
        'gene effect'],
       'dataset_count': 6740,
       'disease_count': 752,
       'tissue_count': 60,
       'organism_count': 22,
       'cell_line_count': 347,
       'cell_type_count': 310,
       'drug_count': 4704,
       'data_type_count': 12,
       'data_source_count': 10,
       'sample_count': 143535,
       'normal_sample_count': 110202},
      {'repo_name': 'cbioportal',
       'repo_id': '1623986995264',
       'indexes': {'gct_metadata': 'cbioportal_gct_metadata',
        'h5ad_metadata': 'cbioportal_h5ad_metadata',
        'csv': 'cbioportal_csv',
        'files': 'cbioportal_files',
        'json': 'cbioportal_json',
        'ipynb': 'cbioportal_ipynb',
        'gct_data': 'cbioportal_gct_data',
        'h5ad_data': 'cbioportal_h5ad_data'},
       'diseases': ['prostatic neoplasms',
        'adenocarcinoma of lung',
        'carcinoma, ductal, breast',
        'breast neoplasms',
        'colorectal neoplasms',
        'leukemia, myeloid, acute',
        'melanoma',
        'leukemia, b-cell',
        'glioblastoma',
        'lymphoma, large b-cell, diffuse',
        'carcinoma, adenoid cystic',
        'cholangiocarcinoma',
        'urinary bladder neoplasms',
        'esophageal neoplasms',
        'pancreatic neoplasms',
        'carcinoma, non-small-cell lung',
        'neuroblastoma',
        'leukemia, lymphocytic, chronic, b-cell',
        'astrocytoma',
        'neoplasms, unknown primary'],
       'organisms': ['homo sapiens'],
       'sources': ['cbioportal'],
       'datatypes': ['mutation',
        'copy number variation',
        'fusion',
        'transcriptomics',
        'methylation'],
       'dataset_count': 116760,
       'disease_count': 346,
       'tissue_count': 141,
       'organism_count': 1,
       'cell_line_count': 1580,
       'cell_type_count': 1,
       'drug_count': 1,
       'data_type_count': 5,
       'data_source_count': 1,
       'sample_count': 58994,
       'normal_sample_count': 0},
      {'repo_name': 'depmap',
       'repo_id': '1612338998334',
       'indexes': {'gct_metadata': 'depmap_gct_metadata',
        'h5ad_metadata': 'depmap_h5ad_metadata',
        'csv': 'depmap_csv',
        'files': 'depmap_files',
        'json': 'depmap_json',
        'ipynb': 'depmap_ipynb',
        'gct_data': 'depmap_gct_data',
        'h5ad_data': 'depmap_h5ad_data'},
       'diseases': ['urinary bladder neoplasms',
        'adenocarcinoma of lung',
        'breast neoplasms',
        'melanoma',
        'squamous cell carcinoma of head and neck',
        'glioblastoma',
        'colorectal neoplasms',
        'neuroblastoma',
        'pancreatic neoplasms',
        'stomach neoplasms',
        'liver neoplasms',
        'esophageal squamous cell carcinoma',
        'multiple myeloma',
        'neoplasms, squamous cell',
        'endometrial neoplasms',
        'lung neoplasms',
        'carcinoma, pancreatic ductal',
        'lymphoma, non-hodgkin',
        'small cell lung carcinoma',
        'ovarian neoplasms'],
       'organisms': ['homo sapiens'],
       'sources': ['depmap'],
       'datatypes': ['gene dependency', 'drug screens', 'gene effect', 'rnai'],
       'dataset_count': 32248,
       'disease_count': 130,
       'tissue_count': 48,
       'organism_count': 1,
       'cell_line_count': 1406,
       'cell_type_count': 1,
       'drug_count': 0,
       'data_type_count': 4,
       'data_source_count': 1,
       'sample_count': 4465,
       'normal_sample_count': 0},
      {'repo_name': 'pcd',
       'repo_id': '1622113130397',
       'indexes': {'gct_metadata': 'pcd_gct_metadata',
        'h5ad_metadata': 'pcd_h5ad_metadata',
        'csv': 'pcd_csv',
        'files': 'pcd_files',
        'json': 'pcd_json',
        'ipynb': 'pcd_ipynb',
        'gct_data': 'pcd_gct_data',
        'h5ad_data': 'pcd_h5ad_data'},
       'diseases': ['none',
        'adenocarcinoma',
        'carcinoma, squamous cell',
        'melanoma',
        'squamous cell carcinoma of head and neck',
        'neoplasms, squamous cell',
        'mesothelioma',
        'neuroblastoma',
        'sarcoma',
        'lymphoma, non-hodgkin',
        'carcinoma, renal cell',
        'melanoma, amelanotic',
        'esophageal squamous cell carcinoma',
        'carcinoma, adenosquamous',
        'glioblastoma',
        'carcinoma, endometrioid',
        'adenocarcinoma, mucinous',
        'adenocarcinoma of lung',
        'chondrosarcoma',
        'sarcoma, synovial'],
       'organisms': ['homo sapiens'],
       'sources': ['pharmacodb'],
       'datatypes': ['drug response'],
       'dataset_count': 19501,
       'disease_count': 133,
       'tissue_count': 34,
       'organism_count': 1,
       'cell_line_count': 1400,
       'cell_type_count': 1,
       'drug_count': 749,
       'data_type_count': 1,
       'data_source_count': 1,
       'sample_count': 653500,
       'normal_sample_count': 262},
      {'repo_name': 'lincs',
       'repo_id': '32',
       'indexes': {'gct_metadata': 'lincs_gct_metadata',
        'h5ad_metadata': 'lincs_h5ad_metadata',
        'csv': 'lincs_csv',
        'files': 'lincs_files',
        'ipynb': 'lincs_ipynb',
        'gct_data': 'lincs_gct_data',
        'h5ad_data': 'lincs_h5ad_data'},
       'diseases': ['prostatic neoplasms',
        'normal',
        'colorectal neoplasms',
        'adenocarcinoma of lung',
        'breast neoplasms',
        'melanoma, amelanotic',
        'hepatoblastoma',
        'carcinoma, pancreatic ductal',
        'adenocarcinoma',
        'pancreatic neoplasms',
        'colonic neoplasms',
        'not available',
        'leukemia, monocytic, acute',
        'endometrial neoplasms',
        'carcinoma, large cell',
        'melanoma',
        'adenocarcinoma, mucinous',
        'small cell lung carcinoma',
        'leukemia, myeloid, acute',
        'cystadenocarcinoma, mucinous'],
       'organisms': ['homo sapiens'],
       'sources': ['geo, lincs'],
       'datatypes': ['transcriptomics'],
       'dataset_count': 158254,
       'disease_count': 34,
       'tissue_count': 21,
       'organism_count': 1,
       'cell_line_count': 84,
       'cell_type_count': 2,
       'drug_count': 20347,
       'data_type_count': 1,
       'data_source_count': 1,
       'sample_count': 1368466,
       'normal_sample_count': 187120},
      {'repo_name': 'metabolomics',
       'repo_id': '23',
       'indexes': {'gct_metadata': 'metabolomics_gct_metadata',
        'h5ad_metadata': 'metabolomics_h5ad_metadata',
        'csv': 'metabolomics_csv',
        'files': 'metabolomics_files',
        'ipynb': 'metabolomics_ipynb',
        'gct_data': 'metabolomics_gct_data',
        'h5ad_data': 'metabolomics_h5ad_data'},
       'diseases': ['normal',
        'neoplasms',
        'diabetes mellitus',
        'obesity',
        'liver diseases',
        'cardiovascular diseases',
        'malaria',
        'heart diseases',
        'inflammation',
        'asthma',
        'eye diseases',
        'carcinoma, hepatocellular',
        'diabetes mellitus, type 2',
        'kidney diseases',
        'metabolic syndrome',
        'hyperglycemia',
        'insulin resistance',
        'wounds and injuries',
        'fibrosis',
        'glucose intolerance'],
       'organisms': ['homo sapiens',
        'mus musculus',
        'rattus norvegicus',
        'arabidopsis thaliana',
        'none',
        'bos taurus',
        'escherichia coli',
        'plasmodium falciparum',
        'ovis aries',
        'saccharomyces cerevisiae',
        'trypanosoma brucei',
        'canis lupus familiaris',
        'solanum lycopersicum',
        'zea mays',
        'brassica napus',
        'macaca mulatta',
        'triticum aestivum',
        'sus scrofa domesticus',
        'thalassiosira pseudonana',
        'caenorhabditis elegans'],
       'sources': ['metabolomics workbench', 'metabolights', 'publication', 'geo'],
       'datatypes': ['metabolomics', 'lipidomics', 'single cell'],
       'dataset_count': 1782,
       'disease_count': 215,
       'tissue_count': 135,
       'organism_count': 184,
       'cell_line_count': 24,
       'cell_type_count': 23,
       'drug_count': 67,
       'data_type_count': 3,
       'data_source_count': 4,
       'sample_count': 90845,
       'normal_sample_count': 0},
      {'repo_name': 'immport',
       'repo_id': '1621422280385',
       'indexes': {'gct_metadata': 'immport_gct_metadata',
        'h5ad_metadata': 'immport_h5ad_metadata',
        'csv': 'immport_csv',
        'files': 'immport_files',
        'json': 'immport_json',
        'ipynb': 'immport_ipynb',
        'gct_data': 'immport_gct_data',
        'h5ad_data': 'immport_h5ad_data'},
       'diseases': ['normal',
        'diabetes mellitus, type 1',
        'kidney diseases',
        'renal insufficiency',
        'fused kidney',
        'anthrax',
        'neoplasms',
        'kidney failure, chronic',
        'virus diseases',
        'covid-19',
        'kaposi varicelliform eruption',
        'dermatitis, atopic',
        'fibrosis',
        'lymphoma, non-hodgkin',
        'addison disease',
        'metabolic diseases',
        'lupus erythematosus, systemic',
        'smallpox',
        'heart failure',
        'influenza, human'],
       'organisms': ['homo sapiens', 'mus musculus'],
       'sources': ['immport'],
       'datatypes': ['lab measurement', 'proteomics', 'titer', 'pcr', 'cytometry'],
       'dataset_count': 209432,
       'disease_count': 86,
       'tissue_count': 10,
       'organism_count': 2,
       'cell_line_count': 1,
       'cell_type_count': 2,
       'drug_count': 47,
       'data_type_count': 5,
       'data_source_count': 1,
       'sample_count': 51044,
       'normal_sample_count': 25886},
      {'repo_name': 'transcriptomics__cyt',
       'repo_id': '1612862450692',
       'indexes': {'gct_metadata': 'transcriptomics__cyt_gct_metadata',
        'h5ad_metadata': 'transcriptomics__cyt_h5ad_metadata',
        'csv': 'transcriptomics__cyt_csv',
        'files': 'transcriptomics__cyt_files',
        'json': 'transcriptomics__cyt_json',
        'ipynb': 'transcriptomics__cyt_ipynb',
        'gct_data': 'transcriptomics__cyt_gct_data',
        'h5ad_data': 'transcriptomics__cyt_h5ad_data'},
       'diseases': ['normal',
        'ulcerative colitis',
        'crohn disease',
        'breast carcinoma',
        'colorectal carcinoma',
        'melanoma',
        'colon carcinoma',
        'osteoarthritis',
        'covid-19',
        'endometrial carcinoma',
        'gastroenteropancreatic neuroendocrine',
        'lung adenocarcinoma',
        'non-small cell lung carcinoma',
        'pancreatic adenocarcinoma',
        'renal carcinoma',
        'salmonella enterica',
        'salmonella infection'],
       'organisms': ['homo sapiens', 'mus musculus', 'rattus rattus'],
       'sources': ['gene expression omnibus (geo)', 'arrayexpress', 'ebi'],
       'datatypes': ['transcriptomics', 'single cell'],
       'dataset_count': 70,
       'disease_count': 17,
       'tissue_count': 33,
       'organism_count': 3,
       'cell_line_count': 0,
       'cell_type_count': 3,
       'drug_count': 0,
       'data_type_count': 2,
       'data_source_count': 3,
       'sample_count': 3021,
       'normal_sample_count': 0},
      {'repo_name': 'ukbiobank',
       'repo_id': '1638762466067',
       'indexes': {'gct_metadata': 'ukbiobank_gct_metadata',
        'h5ad_metadata': 'ukbiobank_h5ad_metadata',
        'csv': 'ukbiobank_csv',
        'files': 'ukbiobank_files',
        'json': 'ukbiobank_json',
        'ipynb': 'ukbiobank_ipynb',
        'gct_data': 'ukbiobank_gct_data',
        'h5ad_data': 'ukbiobank_h5ad_data'},
       'diseases': ['none'],
       'organisms': ['homo sapiens'],
       'sources': [],
       'datatypes': ['gwas'],
       'dataset_count': 362349,
       'disease_count': 1,
       'tissue_count': 1,
       'organism_count': 1,
       'cell_line_count': 1,
       'cell_type_count': 0,
       'drug_count': 1,
       'data_type_count': 1,
       'data_source_count': 0,
       'sample_count': 0,
       'normal_sample_count': 0},
      {'repo_name': 'exelixis',
       'repo_id': '1649172174566',
       'indexes': {'gct_metadata': 'exelixis_gct_metadata',
        'h5ad_metadata': 'exelixis_h5ad_metadata',
        'csv': 'exelixis_csv',
        'files': 'exelixis_files',
        'json': 'exelixis_json',
        'ipynb': 'exelixis_ipynb',
        'gct_data': 'exelixis_gct_data',
        'h5ad_data': 'exelixis_h5ad_data'},
       'diseases': ['carcinoma, hepatocellular'],
       'organisms': ['homo sapiens'],
       'sources': ['geo'],
       'datatypes': ['transcriptomics'],
       'dataset_count': 5,
       'disease_count': 1,
       'tissue_count': 2,
       'organism_count': 1,
       'cell_line_count': 1,
       'cell_type_count': 1,
       'drug_count': 3,
       'data_type_count': 1,
       'data_source_count': 1,
       'sample_count': 484,
       'normal_sample_count': 85},
      {'repo_name': 'bbio',
       'repo_id': '1647250357385',
       'indexes': {'gct_metadata': 'bbio_gct_metadata',
        'h5ad_metadata': 'bbio_h5ad_metadata',
        'csv': 'bbio_csv',
        'files': 'bbio_files',
        'json': 'bbio_json',
        'ipynb': 'bbio_ipynb',
        'gct_data': 'bbio_gct_data',
        'h5ad_data': 'bbio_h5ad_data'},
       'diseases': ['leukemia, myeloid, acute', 'normal'],
       'organisms': ['homo sapiens'],
       'sources': ['branchbio'],
       'datatypes': ['single cell multiomics'],
       'dataset_count': 7,
       'disease_count': 2,
       'tissue_count': 2,
       'organism_count': 1,
       'cell_line_count': 1,
       'cell_type_count': 2,
       'drug_count': 0,
       'data_type_count': 1,
       'data_source_count': 1,
       'sample_count': 0,
       'normal_sample_count': 0},
      {'repo_name': 'sc_data_lake',
       'repo_id': '17',
       'indexes': {'gct_metadata': 'sc_data_lake_gct_metadata',
        'h5ad_metadata': 'sc_data_lake_h5ad_metadata',
        'csv': 'sc_data_lake_csv',
        'files': 'sc_data_lake_files',
        'ipynb': 'sc_data_lake_ipynb',
        'gct_data': 'sc_data_lake_gct_data',
        'h5ad_data': 'sc_data_lake_h5ad_data'},
       'diseases': ['normal',
        'neoplasms',
        'breast neoplasms',
        'melanoma',
        'covid-19',
        'obesity',
        'colorectal neoplasms',
        'carcinoma, non-small-cell lung',
        'glioblastoma',
        'autoimmune diseases',
        'diabetes mellitus',
        'leukemia, myeloid, acute',
        'carcinoma, hepatocellular',
        'alzheimer disease',
        'adenocarcinoma of lung',
        'multiple sclerosis',
        'prostatic neoplasms',
        'diabetes mellitus, type 2',
        'non-alcoholic fatty liver disease',
        'brain neoplasms'],
       'organisms': ['mus musculus',
        'homo sapiens',
        'none',
        'danio rerio',
        'macaca mulatta',
        'mouse',
        'nan',
        'homo sapiens,mus musculus',
        'macaca fascicularis',
        'rattus norvegicus',
        'sus scrofa',
        'drosophila melanogaster',
        'gallus gallus',
        'homo',
        'homo sapiens,rattus norvegicus',
        'mesocricetus auratus',
        'mus musculus domesticus',
        'other sequences'],
       'sources': ['geo',
        'scp',
        'expression atlas',
        'humancellatlas',
        'gene expression omnibus (geo)',
        'publication',
        'zenodo'],
       'datatypes': ['single cell'],
       'dataset_count': 3129,
       'disease_count': 786,
       'tissue_count': 537,
       'organism_count': 18,
       'cell_line_count': 97,
       'cell_type_count': 719,
       'drug_count': 133,
       'data_type_count': 1,
       'data_source_count': 7,
       'sample_count': 355001,
       'normal_sample_count': 0},
      {'repo_name': 'tcga',
       'repo_id': '15',
       'indexes': {'gct_metadata': 'tcga_gct_metadata',
        'h5ad_metadata': 'tcga_h5ad_metadata',
        'csv': 'tcga_csv',
        'files': 'tcga_files',
        'ipynb': 'tcga_ipynb',
        'gct_data': 'tcga_gct_data',
        'h5ad_data': 'tcga_h5ad_data'},
       'diseases': ['breast neoplasms',
        'clear-cell metastatic renal cell carcinoma',
        'squamous cell carcinoma of head and neck',
        'endometrial neoplasms',
        'colorectal neoplasms',
        'adenocarcinoma of lung',
        'glioma',
        'stomach neoplasms',
        'urinary bladder neoplasms',
        'prostatic neoplasms',
        'neoplasms, squamous cell',
        'cystadenocarcinoma, serous',
        'carcinoma, hepatocellular',
        'thyroid neoplasms',
        'melanoma',
        'carcinoma, renal cell',
        'uterine cervical neoplasms',
        'sarcoma',
        'glioblastoma',
        'rectal neoplasms'],
       'organisms': ['homo sapiens'],
       'sources': ['tcga'],
       'datatypes': ['transcriptomics',
        'mirna',
        'copy number variation',
        'mutation',
        'methylation',
        'proteomics'],
       'dataset_count': 55277,
       'disease_count': 41,
       'tissue_count': 62,
       'organism_count': 1,
       'cell_line_count': 1,
       'cell_type_count': 1,
       'drug_count': 703,
       'data_type_count': 6,
       'data_source_count': 1,
       'sample_count': 0,
       'normal_sample_count': 0},
      {'repo_name': 'etx',
       'repo_id': '1641883311001',
       'indexes': {'gct_metadata': 'etx_gct_metadata',
        'h5ad_metadata': 'etx_h5ad_metadata',
        'csv': 'etx_csv',
        'files': 'etx_files',
        'json': 'etx_json',
        'ipynb': 'etx_ipynb',
        'gct_data': 'etx_gct_data',
        'h5ad_data': 'etx_h5ad_data'},
       'diseases': ['non-alcoholic fatty liver disease',
        'obesity',
        'diabetes mellitus, type 2',
        'fatty liver',
        'insulin resistance',
        'normal',
        'multiple organ failure',
        'abdominal',
        'chemical and drug induced liver injury',
        'myotonic dystrophy',
        'carcinoma',
        'cholangitis, sclerosing',
        'end stage liver disease',
        'gallstones',
        'hemochromatosis',
        'hepatitis',
        'hepatitis c',
        'hepatitis, alcoholic',
        'hepatitis, autoimmune',
        'hepatocellular'],
       'organisms': ['homo sapiens'],
       'sources': ['geo',
        'metabolomics workbench',
        'arrayexpress',
        'metabolights',
        'ncbi'],
       'datatypes': ['transcriptomics',
        'metabolomics',
        'lipidomics',
        'methylation'],
       'dataset_count': 98,
       'disease_count': 28,
       'tissue_count': 13,
       'organism_count': 1,
       'cell_line_count': 3,
       'cell_type_count': 17,
       'drug_count': 12,
       'data_type_count': 4,
       'data_source_count': 5,
       'sample_count': 1564,
       'normal_sample_count': 767},
      {'repo_name': 'ngj',
       'repo_id': '1618578954468',
       'indexes': {'gct_metadata': 'ngj_gct_metadata',
        'h5ad_metadata': 'ngj_h5ad_metadata',
        'csv': 'ngj_csv',
        'files': 'ngj_files',
        'json': 'ngj_json',
        'ipynb': 'ngj_ipynb',
        'gct_data': 'ngj_gct_data',
        'h5ad_data': 'ngj_h5ad_data'},
       'diseases': ['none',
        'endometriosis',
        'smith-magenis',
        'tay–sachs',
        'endometriosis, pcos, healthy'],
       'organisms': ['homo sapiens'],
       'sources': ['propreitary'],
       'datatypes': ['mutation', 'transcriptomics', 'mirna'],
       'dataset_count': 18,
       'disease_count': 5,
       'tissue_count': 5,
       'organism_count': 1,
       'cell_line_count': 1,
       'cell_type_count': 2,
       'drug_count': 1,
       'data_type_count': 3,
       'data_source_count': 1,
       'sample_count': 1220,
       'normal_sample_count': 0},
      {'repo_name': 'gtex',
       'repo_id': '14',
       'indexes': {'gct_metadata': 'gtex_gct_metadata',
        'h5ad_metadata': 'gtex_h5ad_metadata',
        'csv': 'gtex_csv',
        'files': 'gtex_files',
        'ipynb': 'gtex_ipynb',
        'gct_data': 'gtex_gct_data',
        'h5ad_data': 'gtex_h5ad_data'},
       'diseases': ['normal'],
       'organisms': ['homo sapiens'],
       'sources': ['gtex'],
       'datatypes': ['transcriptomics'],
       'dataset_count': 30,
       'disease_count': 1,
       'tissue_count': 30,
       'organism_count': 1,
       'cell_line_count': 1,
       'cell_type_count': 1,
       'drug_count': 1,
       'data_type_count': 1,
       'data_source_count': 1,
       'sample_count': 17381,
       'normal_sample_count': 0},
      {'repo_name': 'gnomad',
       'repo_id': '1628836648493',
       'indexes': {'gct_metadata': 'gnomad_gct_metadata',
        'h5ad_metadata': 'gnomad_h5ad_metadata',
        'csv': 'gnomad_csv',
        'files': 'gnomad_files',
        'json': 'gnomad_json',
        'ipynb': 'gnomad_ipynb',
        'gct_data': 'gnomad_gct_data',
        'h5ad_data': 'gnomad_h5ad_data'},
       'diseases': ['none'],
       'organisms': ['homo sapiens'],
       'sources': [],
       'datatypes': ['gwas'],
       'dataset_count': 196744,
       'disease_count': 1,
       'tissue_count': 1,
       'organism_count': 1,
       'cell_line_count': 1,
       'cell_type_count': 0,
       'drug_count': 1,
       'data_type_count': 1,
       'data_source_count': 0,
       'sample_count': 0,
       'normal_sample_count': 0},
      {'repo_name': 'geo_raw_counts',
       'repo_id': '1647341066415',
       'indexes': {'gct_metadata': 'geo_raw_counts_gct_metadata',
        'h5ad_metadata': 'geo_raw_counts_h5ad_metadata',
        'csv': 'geo_raw_counts_csv',
        'files': 'geo_raw_counts_files',
        'json': 'geo_raw_counts_json',
        'ipynb': 'geo_raw_counts_ipynb',
        'gct_data': 'geo_raw_counts_gct_data',
        'h5ad_data': 'geo_raw_counts_h5ad_data'},
       'diseases': ['normal',
        'neoplasms',
        'breast neoplasms',
        'leukemia, myeloid, acute',
        'obesity',
        'melanoma',
        'prostatic neoplasms',
        'carcinoma, hepatocellular',
        'glioblastoma',
        'autoimmune diseases',
        'colorectal neoplasms',
        'alzheimer disease',
        'leukemia',
        'adenocarcinoma of lung',
        'diabetes mellitus',
        'colonic neoplasms',
        'huntington disease',
        'neuroblastoma',
        'neurodegenerative diseases',
        'diabetes mellitus, type 2'],
       'organisms': ['mus musculus',
        'homo sapiens',
        'caenorhabditis elegans',
        'escherichia coli',
        'danio rerio',
        'rattus norvegicus',
        'arabidopsis thaliana',
        'saccharomyces cerevisiae',
        'human herpesvirus 4'],
       'sources': ['geo'],
       'datatypes': ['raw counts transcriptomics'],
       'dataset_count': 10827,
       'disease_count': 1306,
       'tissue_count': 537,
       'organism_count': 9,
       'cell_line_count': 1316,
       'cell_type_count': 517,
       'drug_count': 238,
       'data_type_count': 1,
       'data_source_count': 1,
       'sample_count': 149895,
       'normal_sample_count': 123590}]}



### omixatlas_summary
### input
repo_id or repo key
### output
it will return a object which contain information about repo
<a id="omixatlas_summary"></a>


```python
omixatlas.omixatlas_summary(1650348922627)
```




    {'data': {'repo_name': 'atavistik',
      'repo_id': '1650348922627',
      'indexes': {'gct_metadata': 'atavistik_gct_metadata',
       'h5ad_metadata': 'atavistik_h5ad_metadata',
       'csv': 'atavistik_csv',
       'files': 'atavistik_files',
       'json': 'atavistik_json',
       'ipynb': 'atavistik_ipynb',
       'gct_data': 'atavistik_gct_data',
       'h5ad_data': 'atavistik_h5ad_data'},
      'diseases': ['none'],
      'organisms': ['none'],
      'sources': ['none'],
      'datatypes': [],
      'dataset_count': 1,
      'disease_count': 1,
      'tissue_count': 1,
      'organism_count': 1,
      'cell_line_count': 0,
      'cell_type_count': 0,
      'drug_count': 0,
      'data_type_count': 0,
      'data_source_count': 1,
      'sample_count': 0,
      'normal_sample_count': 0}}



### query_metadata
### input :
query (str) : sql query on omixatlas for example - “SELECT * FROM liveromix_atlas.datasets”.<br>
experimental_features (optional): this section includes in querying metadata. <br>
query_api_version (str) (optional): v1 or v2.<br>
page_size (int) (optional): page size for query.<br>
for more information - https://vito39.github.io/testing_repo_2/polly.html#polly.omixatlas.OmixAtlas.query_metadata
### output :
It will return a table that will contain metadata (for example- disease,total_num_cells) and datasets that 
satisfied the sql query.
<a id="query_metadata"></a>


```python
query = "SELECT * FROM geo.datasets LIMIT 20"
omixatlas.query_metadata(query)
```

    Query execution succeeded
    Fetched 20 rows





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>publication_name</th>
      <th>tissue</th>
      <th>dataset_source</th>
      <th>description</th>
      <th>organism</th>
      <th>year</th>
      <th>disease</th>
      <th>operation</th>
      <th>platform</th>
      <th>dataset_id</th>
      <th>...</th>
      <th>kw_region</th>
      <th>kw_location</th>
      <th>kw_timestamp</th>
      <th>experimental_design</th>
      <th>author</th>
      <th>abstract</th>
      <th>type</th>
      <th>manually_curated</th>
      <th>file_type</th>
      <th>source_process</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>none</td>
      <td>[None]</td>
      <td>GEO</td>
      <td>Inhibition of NF-ÎºB-dependent signaling enhan...</td>
      <td>[Homo sapiens]</td>
      <td>2018</td>
      <td>[Melanoma, Uveal melanoma]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE124059_GPL11154</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622402236</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>30518681</td>
      <td>[bone marrow]</td>
      <td>GEO</td>
      <td>Human Bone Marrow Assessment by Single Cell RN...</td>
      <td>[Homo sapiens]</td>
      <td>2018</td>
      <td>[Normal]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE120444_GPL21290</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622405780</td>
      <td>{'categorical_variables': {'age': [{'name': '2...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>31350386</td>
      <td>[joint, knee]</td>
      <td>GEO</td>
      <td>Stabilizing Heterochromatin by DGCR8 Alleviate...</td>
      <td>[Mus musculus]</td>
      <td>2018</td>
      <td>[Osteoarthritis, DiGeorge Syndrome]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE121029_GPL21273</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622407836</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>28903501</td>
      <td>[liver]</td>
      <td>GEO</td>
      <td>Liver lncRNA gene expression in response to CA...</td>
      <td>[Mus musculus]</td>
      <td>Jun 17 2019</td>
      <td>[Normal]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE120851_GPL13112</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622403758</td>
      <td>{'categorical_variables': {'age': [{'name': '8...</td>
      <td>David,J.,Waxman</td>
      <td>Gene expression in livers of male and female m...</td>
      <td>Non-coding RNA profiling by high throughput se...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>31365869</td>
      <td>[tibialis anterior]</td>
      <td>GEO</td>
      <td>RNAi Screening for Ubiquitin Ligases that Regu...</td>
      <td>[Mus musculus]</td>
      <td>2018</td>
      <td>[Myostatin-related muscle hypertrophy]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE126922_GPL17021</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622447941</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>30540963</td>
      <td>[muscle, motoneuron]</td>
      <td>GEO</td>
      <td>RNAseq of fluidically isolated human and mouse...</td>
      <td>[Mus musculus]</td>
      <td>2018</td>
      <td>[Amyotrophic Lateral Sclerosis]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE121069_GPL17021</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622444678</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>30707899</td>
      <td>[None]</td>
      <td>GEO</td>
      <td>Loss of primary cilia drives switching from He...</td>
      <td>[Mus musculus]</td>
      <td>2018</td>
      <td>[Carcinoma, Basal Cell]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE120954_GPL13112</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622444725</td>
      <td>{'categorical_variables': {'agent': [{'name': ...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7</th>
      <td>31160601</td>
      <td>[None]</td>
      <td>GEO</td>
      <td>Transcriptional profiling of Ampk-deficient B ...</td>
      <td>[Mus musculus]</td>
      <td>Jun 16 2019</td>
      <td>[Normal]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE121025_GPL24247</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622446965</td>
      <td>NaN</td>
      <td>Fasih,Mubtasim,Ahsan</td>
      <td>5’-AMP-Activated Protein Kinase (Ampk) is an e...</td>
      <td>Expression profiling by high throughput sequen...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>none</td>
      <td>[hippocampus]</td>
      <td>GEO</td>
      <td>Altered expression of signaling pathways regul...</td>
      <td>[Homo sapiens]</td>
      <td>2018</td>
      <td>[Seizures, Epilepsy, Temporal Lobe]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE127871_GPL16791</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622443907</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>31591481</td>
      <td>[None]</td>
      <td>GEO</td>
      <td>Oncogenic HOXB8 is driven by MYC-regulated sup...</td>
      <td>[Homo sapiens]</td>
      <td>Mar 01 2020</td>
      <td>[Colonic Neoplasms]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE121207_GPL23227</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622457503</td>
      <td>{'categorical_variables': {'cell_line': [{'nam...</td>
      <td>Xingsheng,,Shu</td>
      <td>HOXB8 acts as a transcription facor, thus we k...</td>
      <td>Expression profiling by high throughput sequen...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>10</th>
      <td>31442403</td>
      <td>[spinal cord, bone marrow, liver]</td>
      <td>GEO</td>
      <td>Dietary intake regulates the circulating pro-i...</td>
      <td>[Mus musculus]</td>
      <td>2018</td>
      <td>[Normal]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE126899_GPL19057</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622450144</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>11</th>
      <td>none</td>
      <td>[None]</td>
      <td>GEO</td>
      <td>RNAseq analysis of glomerular transcriptome of...</td>
      <td>[Mus musculus]</td>
      <td>2018</td>
      <td>[Glomerulonephritis, Proteinuria, Renal Insuff...</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE126217_GPL13112</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622503324</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>12</th>
      <td>31444334</td>
      <td>[None]</td>
      <td>GEO</td>
      <td>Single-cell profiling guided combinatorial imm...</td>
      <td>[Mus musculus]</td>
      <td>Sep 03 2019</td>
      <td>[Triple Negative Breast Neoplasms]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE122336_GPL17021</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622511647</td>
      <td>{'categorical_variables': {'genotype': [{'name...</td>
      <td>Qingfei,,Wang</td>
      <td>Trastuzumab (Herceptin™), a humanized monoclon...</td>
      <td>Expression profiling by high throughput sequen...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>13</th>
      <td>none</td>
      <td>[breast]</td>
      <td>GEO</td>
      <td>RNA sequencing of GLO1-depleted MDA-MB-231 bre...</td>
      <td>[Homo sapiens]</td>
      <td>2018</td>
      <td>[Breast Neoplasms]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE122229_GPL18573</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622505579</td>
      <td>{'categorical_variables': {'cancer_type': [{'n...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>14</th>
      <td>30670076</td>
      <td>[None]</td>
      <td>GEO</td>
      <td>Prediction of functional microRNA targets by i...</td>
      <td>[Homo sapiens]</td>
      <td>2018</td>
      <td>[Normal]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE124530_GPL21290</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622579881</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>15</th>
      <td>30814741</td>
      <td>[None]</td>
      <td>GEO</td>
      <td>Gene expression profiles of 35 paired HCC and ...</td>
      <td>[Homo sapiens]</td>
      <td>2018</td>
      <td>[Normal, Carcinoma, Hepatocellular]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>RNASeq</td>
      <td>GSE124535_GPL20795</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647622586359</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>[kw_curated_disease]</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>16</th>
      <td>18537183</td>
      <td>[None]</td>
      <td>GEO</td>
      <td>Gene expression after transfection of IGF-II s...</td>
      <td>[Homo sapiens]</td>
      <td>2018</td>
      <td>[Carcinoma, Hepatocellular]</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>Microarray</td>
      <td>GSE8714_GPL5705</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647620477069</td>
      <td>{'categorical_variables': {'other_0': [{'name'...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>17</th>
      <td>NaN</td>
      <td>[None]</td>
      <td>GEO</td>
      <td>Identification of genes regulated by Rb in wil...</td>
      <td>[Mus musculus]</td>
      <td>NaN</td>
      <td>[Normal]</td>
      <td>NaN</td>
      <td>Microarray</td>
      <td>GSE90571_GPL10787</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647620477228</td>
      <td>{'categorical_variables': {'cell_type': [{'nam...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>gct</td>
      <td>connector</td>
    </tr>
    <tr>
      <th>18</th>
      <td>none</td>
      <td>[tongue]</td>
      <td>GEO</td>
      <td>Dek overexpression under the environment expos...</td>
      <td>[Mus musculus]</td>
      <td>2018</td>
      <td>[Squamous Cell Carcinoma of Head and Neck, Ton...</td>
      <td>{'is_normalized': 'true', 'batch_corrected_var...</td>
      <td>Microarray</td>
      <td>GSE87587_GPL13912</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647620477253</td>
      <td>{'categorical_variables': {'genotype_variation...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>19</th>
      <td>NaN</td>
      <td>[lung]</td>
      <td>GEO</td>
      <td>Examine the expression profiles of lncRNAs in ...</td>
      <td>[Homo sapiens]</td>
      <td>NaN</td>
      <td>[Carcinoma, Squamous Cell]</td>
      <td>NaN</td>
      <td>Microarray</td>
      <td>GSE88862_GPL16956</td>
      <td>...</td>
      <td>us-west-2</td>
      <td>https://discover-prod-datalake-v1.s3-us-west-2...</td>
      <td>1647620504342</td>
      <td>{'categorical_variables': {'age': [{'name': '6...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>gct</td>
      <td>connector</td>
    </tr>
  </tbody>
</table>
<p>20 rows × 43 columns</p>
</div>



### download_data
### input
repo_key (str): repo_id OR repo_name from where the data needs to be downloaded.<br>
dataset_id (str): dataset_id which the user wants to download.
### output
message containing information about dataset
<a id="download_data"></a>


```python
omixatlas.download_data("geo", "GSE124059_GPL11154")
```




    {'data': {'attributes': {'last-modified': '2021-12-22 08:38:05.000000',
       'size': '2.03 MB',
       'download_url': 'https://discover-prod-datalake-v1.s3.amazonaws.com/GEO_data_lake/data/RNASeq/GSE124059/GCT/GSE124059_GPL11154_curated.gct?AWSAccessKeyId=ASIAVRYB5UBIF5PI74HH&Signature=L6HzDXxVubK%2BaJB%2B4WSykrvSjC0%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEBUaCXVzLXdlc3QtMiJHMEUCIDW7yqwmK09n9gGe99ajjMR%2Fhj8%2B4JW2eki%2ByfX87YdfAiEArHENmeeV%2F7C6Z5NFWHXQYk79tBKnqwgTMVOvMkRYnzAqqgIIzv%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARADGgwzODE3MTkyNTcxNjgiDMDWCMFKhrNC46gklSr%2BAVbyNPD%2FLqMzTBp8MomhXIu7SRgE4iclXtWv1OVbgA%2BkrkqSbS6IG2AAfwzmpuKyqz9rbC5q4pD%2BPmLF48dCa9Bey%2B207zDclfGGzmA0NAiBcoLpE0TvYjn1oq4q5hINeIiw5Rx9lMfNGLpOIvIjAYvYCEtsMcqk%2BlqNu2XO6CXPVD0GJ71dIQgqqiPOJb%2F%2BUrXWXlQtbCqIjyD%2FHkCrjdW2%2Bl9pfPeOvYnjpkTK378gXP72V71l4Mmpnl14KalFMae2bO2wIsQeqUZ96S2jqF4xKh92LQk9XbB9WR0%2FvOod2LxZ8wz3g%2BMo488sDmghwDVqPZ7%2BSOPjNyj9yxa2MOq1qJMGOpoBCt%2F2p%2FXoUZwo%2F8uYbC2UBhNaOcK6JJgfU%2BT%2BHpP7RuxusxevIivuPZl1Nvl%2Bncr8Bcl8K4oE5JTKoHH7inB1lROkAoVm2Rz%2FxO8d%2BspBnuVKAMH4ZaCly0vx1LGX%2FA1VdZf9aNRUN5nR%2FPmhbp1iadjcmuw3m%2BFayrOTCUUNlXt1WQsmQt3GCocyU8fi1obr2YidhQFXvO48JQ%3D%3D&Expires=1651127122'}}}



### save_to_workspace
### input :
repo_id (str) : repo id.<br>
dataset_id (str) : dataset id.<br>
workspace_id (str) : workspace id of polly.<br>
workspace_path (str) : path in workspace where you want to save file.<br>
### output :
object containing information about dataset upload.
<a id="save_to_workspace"></a>


```python
omixatlas.save_to_workspace('9', 'GSE124059_GPL11154', 9009, 'data')
```

    INFO:root:Data Saved to workspace=9009





    {'data': {'type': 'workspace-jobs',
      'id': '9/9009',
      'attributes': {'destination-gct': '9009/data/GSE124059_GPL11154_curated.gct',
       'destination-json': '9009/data/GSE124059_GPL11154.json'}}}



### format_converter
### Input:
repo_key (str) : repo_id.<br>
dataset_id (str) : dataset_id.<br>
to(str) : output file format.<br>
### Output:
Message File converted successfully!
<a id="format_converter"></a>


```python
omixatlas.format_converter("cbioportal", "ACC_2019_Mutation_ACYC-FMI-19", "maf")
```

    INFO:cmap_logger:Reading GCT: ACC_2019_Mutation_ACYC-FMI-19.gct
    INFO:root:File converted successfully!


### get_schema
### Input:
repo_key (str) : repo_id OR repo_name. This is a mandatory field.<br>
schema_level (list) : The default value is [‘dataset’, ‘sample’]. The users can use [‘dataset’] OR [‘sample’] to fetch
the schema of dataset OR sample level metadata respectively.<br>
source (str) : is the source from where data is ingested into the Omixatlas.<br>
data_type (str) : is the datatype for which user wants to get the schema for. The default value is ‘all’, which will 
fetch the schema of all datatypes except single cell. To fetch the schema for single cell datatype from an OmixAtlas, 
the user should use ‘single_cell’.<br>
### Output:
It will contain the schema for dataset, sample as dataframe.
{
    'dataset':pd.DataFrame,
    'sample':pd.DataFrame
}
<a id="get_schema"></a>


```python
schema = omixatlas.get_schema("geo", ['dataset', 'sample'], "all", "all")
```


```python
schema.dataset
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Source</th>
      <th>Datatype</th>
      <th>Field Name</th>
      <th>Field Description</th>
      <th>Field Type</th>
      <th>Is Array</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>all</td>
      <td>all</td>
      <td>curated_organism</td>
      <td>Orgnism from which the samples were derived</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>1</th>
      <td>all</td>
      <td>all</td>
      <td>src_uri</td>
      <td>Unique URI derived from data file's S3 location</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>all</td>
      <td>all</td>
      <td>total_num_samples</td>
      <td>Total number of samples in a dataset</td>
      <td>integer</td>
      <td>False</td>
    </tr>
    <tr>
      <th>3</th>
      <td>all</td>
      <td>all</td>
      <td>year</td>
      <td>Year in which the dataset was published</td>
      <td>integer</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>all</td>
      <td>all</td>
      <td>description</td>
      <td>Description of the dataset</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>5</th>
      <td>all</td>
      <td>all</td>
      <td>curated_cell_line</td>
      <td>Cell lines from which the samples were derived...</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>6</th>
      <td>all</td>
      <td>all</td>
      <td>data_table_name</td>
      <td>Name of the data table associated with data file</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>7</th>
      <td>all</td>
      <td>all</td>
      <td>data_table_version</td>
      <td>Current version of the data table associated w...</td>
      <td>integer</td>
      <td>False</td>
    </tr>
    <tr>
      <th>8</th>
      <td>all</td>
      <td>all</td>
      <td>platform</td>
      <td>Platform Accession number signifying the techn...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>9</th>
      <td>all</td>
      <td>all</td>
      <td>timestamp_</td>
      <td>Unix timestamp denoting time of creation for t...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>10</th>
      <td>all</td>
      <td>all</td>
      <td>file_type</td>
      <td>Data file's type</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>11</th>
      <td>all</td>
      <td>all</td>
      <td>publication</td>
      <td>Publication associated with the dataset</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>12</th>
      <td>all</td>
      <td>all</td>
      <td>curated_cell_type</td>
      <td>Types of cell present in the dataset</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>13</th>
      <td>all</td>
      <td>all</td>
      <td>key</td>
      <td>Key to the data file in source package</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>14</th>
      <td>all</td>
      <td>all</td>
      <td>summary</td>
      <td>Summary of the paper</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>15</th>
      <td>all</td>
      <td>all</td>
      <td>src_repo</td>
      <td>Name of the repository this data file originat...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>16</th>
      <td>all</td>
      <td>all</td>
      <td>drug_smiles</td>
      <td>SMILES code of the drug</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>17</th>
      <td>all</td>
      <td>all</td>
      <td>package</td>
      <td>Name of the package this data file was part of</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>18</th>
      <td>all</td>
      <td>all</td>
      <td>file_location</td>
      <td>Unique S3 location for this data file</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>19</th>
      <td>all</td>
      <td>all</td>
      <td>author</td>
      <td>Name of the author who published the dataset</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>20</th>
      <td>all</td>
      <td>all</td>
      <td>dataset_id</td>
      <td>Unique ID assocaited with every dataset</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>21</th>
      <td>all</td>
      <td>all</td>
      <td>curated_drug</td>
      <td>Drugs administered in the samples belonging to...</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>22</th>
      <td>all</td>
      <td>all</td>
      <td>curated_gene</td>
      <td>Gene studied in the dataset</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>23</th>
      <td>all</td>
      <td>all</td>
      <td>curated_disease</td>
      <td>Disease associated with the dataset</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>24</th>
      <td>all</td>
      <td>all</td>
      <td>abstract</td>
      <td>Abstract of the publication assocaited with th...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>25</th>
      <td>all</td>
      <td>all</td>
      <td>version</td>
      <td>Version of data file</td>
      <td>integer</td>
      <td>False</td>
    </tr>
    <tr>
      <th>26</th>
      <td>all</td>
      <td>all</td>
      <td>curated_strain</td>
      <td>Strain of the organism from which samples were...</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>27</th>
      <td>all</td>
      <td>all</td>
      <td>bucket</td>
      <td>S3 bucket in which the data file resides</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>28</th>
      <td>all</td>
      <td>all</td>
      <td>curated_tissue</td>
      <td>Tissue from which the samples were derivved</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>29</th>
      <td>all</td>
      <td>all</td>
      <td>dataset_source</td>
      <td>Source from where the data was fetched</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>30</th>
      <td>all</td>
      <td>all</td>
      <td>data_type</td>
      <td>The type of biomolecular data captured (eg - E...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>31</th>
      <td>all</td>
      <td>all</td>
      <td>overall_design</td>
      <td>Overall Design of the experiment as given by t...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>32</th>
      <td>all</td>
      <td>all</td>
      <td>is_current</td>
      <td>Whether this is the current version of the dat...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>33</th>
      <td>all</td>
      <td>all</td>
      <td>region</td>
      <td>Region (AWS) in which this data is located</td>
      <td>text</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>




```python
schema.sample
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Source</th>
      <th>Datatype</th>
      <th>Field Name</th>
      <th>Field Description</th>
      <th>Field Type</th>
      <th>Is Array</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>all</td>
      <td>all</td>
      <td>growth_protocol_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>all</td>
      <td>all</td>
      <td>src_uri</td>
      <td>Unique URI derived from source data file's S3 ...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>all</td>
      <td>all</td>
      <td>sample_id</td>
      <td>Unique ID associated with every sample</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>3</th>
      <td>all</td>
      <td>all</td>
      <td>curated_gene_modified</td>
      <td>Gene modified through genetic modification</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>4</th>
      <td>all</td>
      <td>all</td>
      <td>dose_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>5</th>
      <td>all</td>
      <td>all</td>
      <td>curated_cohort_name</td>
      <td>Name of the cohort to which the sample belongs</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>6</th>
      <td>all</td>
      <td>all</td>
      <td>curated_control</td>
      <td>Signifies whether the given sample is a contro...</td>
      <td>integer</td>
      <td>False</td>
    </tr>
    <tr>
      <th>7</th>
      <td>all</td>
      <td>all</td>
      <td>src_dataset_id</td>
      <td>Dataset ID of the file this data entity origin...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>8</th>
      <td>all</td>
      <td>all</td>
      <td>extract_protocol_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>9</th>
      <td>all</td>
      <td>all</td>
      <td>characteristics_ch2</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>10</th>
      <td>all</td>
      <td>all</td>
      <td>characteristics_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>11</th>
      <td>all</td>
      <td>all</td>
      <td>extract_protocol_ch2</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>12</th>
      <td>all</td>
      <td>all</td>
      <td>age_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>13</th>
      <td>all</td>
      <td>all</td>
      <td>curated_cell_type</td>
      <td>Types of cell present in the sample</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>14</th>
      <td>all</td>
      <td>all</td>
      <td>sex_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>15</th>
      <td>all</td>
      <td>all</td>
      <td>treatment_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>16</th>
      <td>all</td>
      <td>all</td>
      <td>dataset_id</td>
      <td>Unique ID of the dataset to which the sample b...</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>17</th>
      <td>all</td>
      <td>all</td>
      <td>taxid_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>18</th>
      <td>all</td>
      <td>all</td>
      <td>curated_gene</td>
      <td>Gene of interest in the sample</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>19</th>
      <td>all</td>
      <td>all</td>
      <td>curated_drug</td>
      <td>Drug admistered in the sample</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>20</th>
      <td>all</td>
      <td>all</td>
      <td>version</td>
      <td>Version of data entity</td>
      <td>integer</td>
      <td>False</td>
    </tr>
    <tr>
      <th>21</th>
      <td>all</td>
      <td>all</td>
      <td>label_protocol_ch2</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>22</th>
      <td>all</td>
      <td>all</td>
      <td>label_protocol_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>23</th>
      <td>all</td>
      <td>all</td>
      <td>treatment_protocol_ch2</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>24</th>
      <td>all</td>
      <td>all</td>
      <td>characteristics_ch2_1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>25</th>
      <td>all</td>
      <td>all</td>
      <td>treatment_protocol_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>26</th>
      <td>all</td>
      <td>all</td>
      <td>instrument_model</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>27</th>
      <td>all</td>
      <td>all</td>
      <td>name</td>
      <td>Name of the data entity (local to its source f...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>28</th>
      <td>all</td>
      <td>all</td>
      <td>curated_genetic_modification_type</td>
      <td>Signifies the kind of genetic modification per...</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>29</th>
      <td>all</td>
      <td>all</td>
      <td>bmi_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>30</th>
      <td>all</td>
      <td>all</td>
      <td>data_processing</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>31</th>
      <td>all</td>
      <td>all</td>
      <td>curated_cell_line</td>
      <td>Cell line from which the sample was derived</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>32</th>
      <td>all</td>
      <td>all</td>
      <td>description</td>
      <td>Description of the sample</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>33</th>
      <td>all</td>
      <td>all</td>
      <td>title</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>34</th>
      <td>all</td>
      <td>all</td>
      <td>timestamp_</td>
      <td>Unix timestamp denoting time of creation for t...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>35</th>
      <td>all</td>
      <td>all</td>
      <td>curated_cohort_id</td>
      <td>Numeric ID of the cohort to which the sample b...</td>
      <td>integer</td>
      <td>False</td>
    </tr>
    <tr>
      <th>36</th>
      <td>all</td>
      <td>all</td>
      <td>data_id</td>
      <td>Unique ID for this data entity on Polly</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>37</th>
      <td>all</td>
      <td>all</td>
      <td>src_repo</td>
      <td>Name of the repository this data entity origin...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>38</th>
      <td>all</td>
      <td>all</td>
      <td>id_key</td>
      <td>Name of the key that was used for creation of ...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>39</th>
      <td>all</td>
      <td>all</td>
      <td>gender_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>40</th>
      <td>all</td>
      <td>all</td>
      <td>smoking_status_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>41</th>
      <td>all</td>
      <td>all</td>
      <td>label_ch2</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>42</th>
      <td>all</td>
      <td>all</td>
      <td>curated_disease</td>
      <td>Disease associated with the sample</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>43</th>
      <td>all</td>
      <td>all</td>
      <td>label_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>44</th>
      <td>all</td>
      <td>all</td>
      <td>time_point_ch1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>45</th>
      <td>all</td>
      <td>all</td>
      <td>characteristics_ch1_3</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>46</th>
      <td>all</td>
      <td>all</td>
      <td>characteristics_ch1_2</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>47</th>
      <td>all</td>
      <td>all</td>
      <td>curated_tissue</td>
      <td>Tissue to which the sample belongs</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>48</th>
      <td>all</td>
      <td>all</td>
      <td>curated_drug_smiles_code</td>
      <td>SMILES code of the drug admistered in the sample</td>
      <td>text</td>
      <td>True</td>
    </tr>
    <tr>
      <th>49</th>
      <td>all</td>
      <td>all</td>
      <td>hyb_protocol</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>50</th>
      <td>all</td>
      <td>all</td>
      <td>platform_id</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>51</th>
      <td>all</td>
      <td>all</td>
      <td>is_current</td>
      <td>Whether this is the current version of the dat...</td>
      <td>text</td>
      <td>False</td>
    </tr>
    <tr>
      <th>52</th>
      <td>all</td>
      <td>all</td>
      <td>characteristics_ch1_1</td>
      <td>NA</td>
      <td>text</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>




```python
import json
repo_key = 'any_key'
payload = {
 "repo_id": "any_key",
 "schema_type": "files",
 "created_time": 1649765088197,
 "enabled": True,
 "last_updated_time": 1650421685751,
 "schema": {
  "all": {
    "author": {
     "description": "Name of the author who published the dataset",
     "display_name": "Author",
     "filter_size": 1,
     "is_array": False,
     "is_column": False,
     "is_filter": False,
     "is_keyword": False,
     "original_name": "author",
     "type": "text"
    },
    "bucket": {
     "description": "S3 bucket in which the data file resides",
     "display_name": "Bucket",
     "filter_size": 2000,
     "is_array": False,
     "is_column": False,
     "is_filter": False,
     "is_keyword": True,
     "original_name": "kw_bucket",
     "type": "text"
    },
    "curated_cell_line": {
     "description": "Cell lines from which the samples were derived for this dataset",
     "display_name": "Cell line",
     "filter_size": 1000,
     "is_array": True,
     "is_column": True,
     "is_filter": True,
     "is_keyword": True,
     "original_name": "kw_cell_line",
     "type": "text"
    },
    "curated_cell_type": {
     "description": "Types of cell present in the dataset",
     "display_name": "Cell type",
     "filter_size": 1,
     "is_array": True,
     "is_column": True,
     "is_filter": False,
     "is_keyword": True,
     "original_name": "kw_cell_type",
     "type": "text"
    },
    "curated_disease": {
     "description": "Disease associated with the dataset",
     "display_name": "Disease",
     "filter_size": 3000,
     "is_array": True,
     "is_column": True,
     "is_filter": True,
     "is_keyword": True,
     "original_name": "disease",
     "type": "text"
    },
    "curated_drug": {
     "description": "Drugs administered in the samples belonging to the dataset",
     "display_name": "Drug",
     "filter_size": 3000,
     "is_array": True,
     "is_column": True,
     "is_filter": True,
     "is_keyword": True,
     "original_name": "kw_drug",
     "type": "text"
    },
    "curated_gene": {
     "description": "Gene studied in the dataset",
     "display_name": "Gene",
     "filter_size": 1,
     "is_array": True,
     "is_column": False,
     "is_filter": False,
     "is_keyword": True,
     "original_name": "kw_gene",
     "type": "text"
    },
    "curated_organism": {
     "description": "Orgnism from which the samples were derived",
     "display_name": "Organism",
     "filter_size": 1000,
     "is_array": True,
     "is_column": True,
     "is_filter": True,
     "is_keyword": True,
     "original_name": "organism",
     "type": "text"
    },
      "all": {
     "description": "Orgnism from which the samples were derived",
     "display_name": "Organism",
     "filter_size": 1000,
     "is_array": True,
     "is_column": True,
     "is_filter": True,
     "is_keyword": True,
     "original_name": "organism",
     "type": "text"
    }
   }
  }
 }

```

### insert_schema
### Input :
repo_key: (str) repo_id OR repo_name. This is a mandatory field.<br>
payload: (dict) The payload is a JSON file which should be as per the structure defined for schema. Only data-admin will have the authentication to update the schema.
<a id="insert_schema"></a>


```python
omixatlas.insert_schema(repo_key, payload)
```

### update_schema
### Input :
repo_key (str): repo_id OR repo_name. This is a mandatory field.<br>
payload (dict): The payload is a JSON file which should be as per the structure defined for schema. Only data-admin will have the authentication to update the schema.
<a id="update_schema"></a>


```python
omixatlas.update_schema(repo_key, payload)
```
