# Demo of NLP with IBM Watson

"Natural Language Understanding enables advanced text analysis through natural language processing. The service analyzes unstructured text to extract metadata such as entities, general concepts, keywords, categories, relations, sentiment, and emotion. With custom annotation models developed using Watson Knowledge Studio, you can further customize the service to identify domain-specific entities and relations in your content."
https://github.com/tmarkiewicz/nlpdemo

Documentation: 

1. Create a free IBM Cloud (formerly Bluemix) account here: https://ibm.biz/BdjVVX
2. From the Dashboard, click on the blue "Create+" button
3. From the sidebar, select Watson, and then "Natural Language Understanding"
4. Select the "Lite" plan (gives 30,000 NLU items per month for free) and click "Create"
5. Get your credentials


For the following curl requests, we'll use this initial sentence -- "I drove my friend Mary to the park in my Tesla while listening to music on my iPhone."

### request entities
```shell
curl --user "61100b1a-64ad-482a-be61-018a86a3cca3":"l67YmgA2uQC1" \
"https://gateway.watsonplatform.net/natural-language-understanding/api/v1/analyze?version=2017-02-27&text=I%20drove%20my%20friend%20Mary%20to%20the%20park%20in%20my%20Tesla%20while%20listening%20to%20music%20on%20my%20iPhone.&features=entities"
```

### request entities,sentiment,emotion
```
curl --user "61100b1a-64ad-482a-be61-018a86a3cca3":"l67YmgA2uQC1" "https://gateway.watsonplatform.net/natural-language-unerstanding/api/v1/analyze?version=2017-02-27&text=I%20drove%20my%20friend%20Mary%20to%20the%20park%20in%20my%20Tesla%20while%20listening%20to%20music%20on%20my%20iPhone.&features=entities,sentiment,emotion"
```

### request entities,sentiment,emotion,keywords
```
curl --user "61100b1a-64ad-482a-be61-018a86a3cca3":"l67YmgA2uQC1" \
"https://gateway.watsonplatform.net/natural-language-understanding/api/v1/analyze?version=2017-02-27&text=I%20drove%20my%20friend%20Mary%20to%20the%20park%20in%20my%20Tesla%20while%20listening%20to%20music%20on%20my%20iPhone.&features=entities,sentiment,emotion,keywords"
```

### request entities,sentiment,emotion,keywords,relations,semantic_roles
```
curl --user "61100b1a-64ad-482a-be61-018a86a3cca3":"l67YmgA2uQC1" \
"https://gateway.watsonplatform.net/natural-language-understanding/api/v1/analyze?version=2017-02-27&text=I%20drove%20my%20friend%20Mary%20to%20the%20park%20in%20my%20Tesla%20while%20listening%20to%20music%20on%20my%20iPhone.&features=entities,sentiment,emotion,keywords,relations,semantic_roles"
```

### change sentiment
New sentence text -- "I drove my mean and angry friend Mary to the park in my Tesla while listening to music on my iPhone."
```
curl --user "61100b1a-64ad-482a-be61-018a86a3cca3":"l67YmgA2uQC1" "https://gateway.watsonplatform.net/natural-language-understanding/api/v1/analyze?version=2017-02-27&text=I%20drove%20my%20mean%20and%20angry%20friend%20Mary%20to%20the%20park%20in%20my%20Tesla%20while%20listening%20to%20music%20on%20my%20iPhone.&features=entities,sentiment,emotion"
```

## Additional resources

