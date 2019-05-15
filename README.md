# RAPIDS Extended Notebooks
## Intro
Welcome to the extended notebooks repo!

The purpose of this collection of notebooks is to help users understand what RAPIDS has to offer, learn how, why, and when including it in data science pipelines makes sense, and help get started using RAPIDS libraries by example. 

Many of these notebooks use additional PyData ecosystem packages, and include code for downloading datasets, thus they require network connectivity. If running on a system with no network access, please use the [core notebooks repo](https://github.com/rapidsai/notebooks).

## Installation

Please use the [BUILD.md](https://github.com/rapidsai/notebooks-extended/tree/master) to check the pre-requisite packages and installation steps.

## Contributing

Please see our [guide for contributing to notebooks-extended](https://github.com/rapidsai/notebooks-extended/blob/master/CONTRIBUTING.md).

## Exploring the Repo

Notebooks live under two subfolders:
- `beginner` - contains notebooks showing “how [to master] RAPIDS”:
    - `basics` - to help you quickly learn the basic RAPIDS APIs.  It contains these notebooks
        - Dask Hello World
        - Getting Started with cuDF
    - `tutorial` - which is a basic tutorial on all the libraries present in RAPIDS.
    
- `advanced` - these notebooks demonstrate "why RAPIDS" by directly comparing compute time between single and multi threaded CPU implementations vs GPU (RAPIDS library) implementations. Of note here is the similarity of RAPIDS APIs to common PyData ecosystem packages like Pandas and scikit-learn. This folder includes the following folders: 
    - E2E: The E2E folder contains end to end notebooks which use the RAPIDS libraries
    - benchmarks: The benchmarks folder contains notebooks which are used to benchmark the cuGraph and cuML algorithms
    - blog notebooks: contains the notebooks mentioned and used in blogs written by RAPIDS
    - conference notebooks
    - examples: contains high level examples for users familiar with RAPIDS libraries

`/data` contains small data samples used for purely functional demonstrations. Some notebooks include cells that download larger datasets from external websites.

The `/data` folder is also symlinked into `/rapids/notebooks/extended/data` so you can browse it from JupyterLab's UI.

# RAPIDS Notebooks-extended

## Beginner Notebooks:
| Folder    | Notebook Title         | Description                                                                                                                                                                                                                   |
|-----------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| basics   | Dask_Hello_World           | This notebook shows how to quickly setup Dask and run a "Hello World" example.                                                                                                                                       |
| basics   | Getting_Started_with_cuDF  | This notebook shows how to get started with GPU DataFrames using cuDF in RAPIDS.                                                                                                                                      |
| tutorial   | 01_Introduction_to_RAPIDS  | This notebook shows at a high level what each of the packages in the RAPIDS are as well as what they do.                                                                                                                                      |
## Advanced Notebooks:
 
| Folder    | Notebook Title         | Description                                                                                                                                                                                                                   |
|-----------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| E2E-> mortgage      | mortgage_e2e            | This is an end to end notebook consisting of `ETL`, `data conversion` and `machine learning for training` operations performed on the mortgage dataset.                                                                               |
| E2E-> mortgage      | mortgage_e2e_deep_learning     | This notebook combines the RAPIDS GPU data processing with a PyTorch deep learning neural network to predict mortgage loan delinquency.                                                                                                                          |
| E2E      | rapids_ml_workflow_demo | This notebook uses random datasets to create an end to end notebook to showcase multiple cuML algorithms and compare them their scikit-learn counterparts                                                                                                                                             |
| benchmarks      | cuml_benchmarks  | The purpose of this notebook is to benchmark all of the single GPU cuML algorithms against their skLearn counterparts, while also providing the ability to find and verify upper bounds.                                                                                                                                          |
| benchmarks-> cugraph_benchmarks      | louvain_benchmark.ipynb   | This notebook benchmarks performance improvement of running the Louvain clustering algorithm within cuGraph against NetworkX.                                                                                                                                                                |
|  benchmarks-> cugraph_benchmarks    |  pagerank_benchmark.ipynb             | This notebook benchmarks performance improvement of running PageRank within cuGraph against NetworkX.                                                                                                                |

### Blog notebooks:
#### Cyber notebooks:
| Folder    | Notebook Title         | Description                                                                                                                                                                                                                   |
|-----------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|flow_classification     | flow_classification_rapids              | This notebook demonstrates how to load netflow data into cuDF and create a multiclass classification model using XGBoost.                                                                                                     |
| network_mapping      | lanl_network_mapping_using_rapids               | This notebook demonstrates how to parse raw windows event logs using cudf and uses cuGraph's pagerank model to build a network graph.                                                                         |
| raw_data_generator      | run_raw_data_generator              | The notebook is used showcase how to generate raw logs from the parsed LANL 2017 json data. The intent is to use the raw data to demonstrate parsing capabilities using cuDF.                       |

#### Databrix Notebooks:
| Folder    | Notebook Title         | Description                                                                                                                                                                                                                   |
|-----------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| databrix   | RAPIDS_PCA_demo_avro_read                | This notebooks purpose is to use a Sample Dataset and compare the CPU vs GPU comparison for the PCA algorithm.                                                                                                                              |
| databrix   | spark_rapids_pca_demo      | Demonstration of using cuGraph to compute vertex similarity using both the Jaccard Similarity and the Overlap Coefficient.                                                                          |

#### Regression Notebooks:
| Folder    | Notebook Title         | Description                                                                                                                                                                                                                   |
|-----------|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| regression   | regression_blog_notebook.ipynb       | Demonstration of using cuGraph to compute the Weighted Jaccard Similarity metric on our training dataset.                                                                                                                     |

### Example Notebooks:
| Folder    | Notebook Title         | Description                                                                                                                                                                                                                   |
|-----------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| examples   | DBSCAN_Demo_FULL               | Demonstrate of using the renumbering features to assigned new vertex IDs to the test graph.  This is useful for when the data sets is  non-contiguous or not integer values                                                   |
| examples   | Dask_with_cuDF_and_XGBoost                    | Demonstration of using cuGraph to computer the Bredth First Search space from a given vertex to all other in our training graph                                                                                               |
| examples   | Dask_with_cuDF_and_XGBoost_Disk                   | Demonstration of using cuGraph to computer the The Shortest Path from a given vertex to all other in our training graph                                                                                                       |
| examples   | One_Hot_Encoding    | Demonstration of using cuGraph to identify clusters in a test graph using Spectral Clustering using both the (A) Balance Cut and (B) the Modularity Maximization quality metrics                                              |
| examples   | PCA_Demo_Full               | Demonstration of using both NetworkX and cuGraph to compute the PageRank of each vertex in our test dataset                                                                                                                   |
| examples   | linear_regression_demo.ipynb     | Demonstration of using both NetworkX and cuGraph  to compute the the number of Triangles in our test dataset                                                                                                                  |
| examples   | ridge_regression_demo.ipynb     | Demonstration of using both NetworkX and cuGraph  to compute the the number of Triangles in our test dataset                                                                                                                  |
| examples   | umap_demo.ipynb     | Demonstration of using both NetworkX and cuGraph  to compute the the number of Triangles in our test dataset                                                                                             

## Additional Information
* The `cuml` folder also includes a small subset of the Mortgage Dataset used in the notebooks and the full image set from the Fashion MNIST dataset.

* `utils`: contains a set of useful scripts for interacting with RAPIDS

* For additional, community driven notebooks, which will include our blogs, tutorials, workflows, and more intricate examples, please see the [Notebooks Extended Repo](https://github.com/rapidsai/notebooks-extended)
