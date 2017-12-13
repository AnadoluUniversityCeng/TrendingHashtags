# TrendingHashtags
The Identification of the Top-N Most Frequent @mentions and #hashtags in the 20 million Turkish Tweets

In this homework, we are going to indentify the top-*N* most frequent @mention and #hashtag entities. 
The dataset contains 20 million Turkish Tweets and can be downloded from [www.kemik.yildiz.edu.tr/data/File/20milyontweet.rar](here).

Please read the write-up: [www.ibm.com/developerworks/community/help/index.jsp?topic=%2Fcom.ibm.lotus.connections.common.help%2Fr_common_mention_hashtag.html](What are @mentions and #hashtags?)

Your project **must** be a valid maven project. `mvn clean package` must produce an executable jar file.
This can be done via maven plugins such as [https://maven.apache.org/plugins/maven-shade-plugin/](shade) or [https://maven.apache.org/plugins/maven-assembly-plugin](assembly) plugin.

Following command line options must be supported. 

Option | Description
------------ | -------------
-n, --number | The number of entities to display.
-e, --entitiy | The name of the entity (e.g., hashtag or mention). 
-r, --reverse | Reverse the comparison (e.g., display most infrequent entities).
-f, --ignore-case |	Fold upper case to lower case characters (e.g., collate #AnadoluÜniversitesi and #anadoluÜniversitesi).

The result will be printed to the standard output in the format of two columns (entity \t frequency) separated by a tab.

P.S. To parse command line arguments, you can use [http://jewelcli.lexicalscope.com](JewelCLI) library.
Hint: [https://docs.oracle.com/javase/tutorial/essential/regex/](Regular Expressions) can be used for detecting entities.
