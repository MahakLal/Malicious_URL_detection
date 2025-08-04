#Malicious URL detection

Problem statement
In this case study, we address the detection of malicious URLs as a multi-class classification problem. In this case study, we classify the raw URLs into different class types such as benign or safe URLs, phishing URLs, malware URLs, or defacement URLs.

Project flow
As we know machine learning algorithms only support numeric inputs so we will create lexical numeric features from input URLs. So the input to machine learning algorithms will be the numeric lexical features rather than actual raw URLs. If you don’t know about lexical features you can refer to the discussion about a lexical feature in StackOverflow.

So, in this case study, we will be using three well-known machine learning ensemble classifiers namely Random Forest, Light GBM, and XGBoost.

Later, we will also compare their performance and plot average feature importance plot to understand which features are important in predicting malicious URLs.

Dataset description
In this case study, we will be using a Malicious URLs dataset of 6,51,191 URLs, out of which 4,28,103 benign or safe URLs, 96,457 defacement URLs, 94,111 phishing URLs, and 32,520 malware URLs.

Now, let’s discuss different types of URLs in our dataset i.e., Benign, Malware, Phishing, and Defacement URLs.

Benign URLs: These are safe to browse URLs. Some of the examples of benign URLs are as follows:
mp3raid.com/music/krizz_kaliko.html
infinitysw.com
google.co.in
myspace.com
Malware URLs: These type of URLs inject malware into the victim’s system once he/she visit such URLs. Some of the examples of malware URLs are as follows:
proplast.co.nz
http://103.112.226.142:36308/Mozi.m
microencapsulation.readmyweather.com
xo3fhvm5lcvzy92q.download
Defacement URLs: Defacement URLs are generally created by hackers with the intention of breaking into a web server and replacing the hosted website with one of their own, using techniques such as code injection, cross-site scripting, etc. Common targets of defacement URLs are religious websites, government websites, bank websites, and corporate websites. Some of the examples of defacement URLs are as follows:
http://www.vnic.co/khach-hang.html
http://www.raci.it/component/user/reset.html
http://www.approvi.com.br/ck.htm
http://www.juventudelirica.com.br/index.html
Phishing URLs: By creating phishing URLs, hackers try to steal sensitive personal or financial information such as login credentials, credit card numbers, internet banking details, etc. Some of the examples of phishing URLs are shown below:
roverslands.net
corporacionrossenditotours.com
http://drive-google-com.fanalav.com/6a7ec96d6a
citiprepaid-salarysea-at.tk
Next, we will plot the word cloud of different types of URLs.

Wordcloud of URLs
The word cloud helps in understanding the pattern of words/tokens in particular target labels.

It is one of the most appealing techniques of natural language processing for understanding the pattern of word distribution.

As we can see in the below figure word cloud of benign URLs is pretty obvious having frequent tokens such as html, com, org, wiki etc. Phishing URLs have frequent tokens as tools, ietf, www, index, battle, net whereas html, org, html are higher frequency tokens as these URLs try to mimick original URLs for deceiving the users.

The word cloud of malware URLs has higher frequency tokens of exe, E7, BB, MOZI. These tokens are also obvious as malware URLs try to install trojans in the form of executable files over the users’ system once the user visits those URLs.

The defacement URLs’ intention is to modify the original website’s code and this is the reason that tokens in its word cloud are more common development terms such as index, php, itemid, https, option, etc.

