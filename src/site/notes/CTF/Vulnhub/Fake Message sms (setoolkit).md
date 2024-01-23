---
{"tags":["walkthrought"],"dg-publish":true,"permalink":"/ctf/vulnhub/fake-message-sms-setoolkit/","dgPassFrontmatter":true,"noteIcon":""}
---

	(social engineering tools kit)
	is not including in update old version can't support now
	use other platform same like setoolkit

	git clone https://github.com/machine1337/fake-sms
	pip install -r requirements.txt
		python3 fakesms.py
	
  
	  https://textbelt.com/


```python
import requestsresp = requests.post('https://textbelt.com/text', {  'phone': '959111111',  'message': 'how are you',  'key': 'textbelt',})print(resp.json())
```



	ကီးနေရာမှာမှာ ပိုက်ဆံပေးပြီး api ကီးထည့်သုံးလည်းရတယ်
	