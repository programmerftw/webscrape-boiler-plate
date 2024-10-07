# webscrape-boiler-plate
Been doing alot of scrapping, saving for future reference!

# import these by defaults
from bs4 import BeautifulSoup
from lxml import etree

# boilerplate code starts from here! contains headers info to get past
url=''

headers={'User-Agent':'Mozilla/5.0 (Windows NT 6.3; Win 64 ; x64) Apple WeKit /537.36(KHTML , like Gecko) Chrome/80.0.3987.162 Safari/537.36'}
webpage=requests.get(url,headers=headers).text

soup=BeautifulSoup(webpage,'lxml')

## now it depends whether to store on array or directly print!

# storing this on .csv
df = pd.DataFrame(info)

df.to_csv('delhi_travel_guide.csv',index=False)


