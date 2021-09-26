# Cloudy with a Chance of Short RTTs: Analyzing Cloud Connectivity in the Internet

The Khang Dang<sup>1</sup>, Nitinder Mohan<sup>1</sup>, Lorenzo Corneo<sup>2</sup>, 
Aleksandr Zavodovski<sup>2</sup>, Jörg Ott<sup>1</sup>, Jussi Kangasharju<sup>3</sup>

<sup>1</sup>Technical University of Munich, <sup>2</sup>Uppsala University, <sup>3</sup>University of Helsinki

---

This repository contains the code to reproduce the results and figures of our publication *Cloudy with a Chance of 
Short RTTs: Analyzing Cloud Connectivity in the Internet* accepted for **ACM IMC 2021**.

To better structure this, all of the code is included in the `Figures.ipynb` file in form of a Jupyter notebook.
We split all of the figures into different cells with headers which provide information about the number of the
figure in the paper as well as a short description of the content.

Also included are two .json-files which are used to convert country codes in the case of `iso3.json` 
(obtained from [here](http://country.io/iso3.json) and to look up additional information and enrich
 the present data in the case of `peeringdb.json` (obtained from [PeeringDB](https://peeringdb.com/api/net)).

---

# Dataset

The data necessary for the plots needs to be downloaded before starting and
is available at [mediaTUM]() with instructions on how to set it up. 
We encourage to cite this dataset in academic publications upon usage.

```
@misc{dataset, 
	author = {Mohan, Nitinder and Dang, The Khang and Corneo, Lorenzo and Zavodovski, Aleksandr and Ott, Jörg and Kangasharju, Jussi},
	title = {Cloudy with a Chance of Short RTTs: Analyzing Cloud Connectivity in the Internet},
	publisher = {Technical University of Munich},
	url = {https://mediatum.ub.tum.de/1624200},
	type = {Dataset},
	year={2021},
	doi = {10.14459/2021mp1624200},
	keywords = {Cloud, Edge computing; Speedchecker; Cloud connectivity; Cloud Reachability; Internet measurements},
	abstract = {Cloud datacenter to user connectivity dataset collected over Speedchecker platform. The dataset accompanies research article 
		   “Cloudy with a Chance of Short RTTs: Analyzing Cloud Connectivity in the Internet” accepted at ACM Internet Measurements Conference (IMC) 2021},
	language = {en},
}
```

Additionally, the dataset from an [earlier publication](https://github.com/lorenzocorneo/surrounded-by-the-clouds) is necessary for certain
figures as well. This dataset is also available at [mediaTUM](https://mediatum.ub.tum.de/1593899).

---

# Usage instructions

These results were created with Python 3.7.7. In addition, several non-default Python libraries were used. These
can be installed with the following command:

```
pip install -r requirements.txt
```

Note that some of the libraries/dependencies (GDAL, Fiona, Cartopy, basemap) might need to be installed manually through wheel files
which are available [here](https://www.lfd.uci.edu/~gohlke/pythonlibs/) for Windows for example. These need to be downloaded 
and can then be installed with:

```
pip install <path/to/wheel/file>
```

It might also be necessary to update pip in order to install all of the libraries. This can be done with:

```
python3 -m pip install --upgrade pip
```

After downloading the necessary datasets and installing these libraries, the code in the notebook can be run after
setting the correct paths for both of the datasets. The resulting figures will then be placed in the `Figs/` folder 
and will be named after the figure identifier used in the paper.