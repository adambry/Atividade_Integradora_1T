# Atividade_Integradora_1T

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from matplotlib import colors
from matplotlib.ticker import PercentFormatter
from ydata_profiling import ProfileReport
import hvplot.pandas
import missingno as msno
import altair as alt

df = pd.read_csv('Bases/cs_bisnode_panel.csv')

df = df.drop(['COGS', 'finished_prod', 'net_dom_sales', 'net_exp_sales', 'wages', 'D'], axis=1)

df = df[df['year']!=2016]

msno.bar(df)


