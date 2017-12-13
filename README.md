# The Identification of the Top-*N* Most Frequent @mentions and #hashtags in the 20 million Turkish Tweets

In this homework, we are going to indentify the top-*N* most frequent @mention and #hashtag entities. 
The dataset contains 20 million Turkish Tweets and can be downloded from [here](www.kemik.yildiz.edu.tr/data/File/20milyontweet.rar).

Please read the write-up: [What are @mentions and #hashtags?](www.ibm.com/developerworks/community/help/index.jsp?topic=%2Fcom.ibm.lotus.connections.common.help%2Fr_common_mention_hashtag.html)

Your project **must** be a valid maven project. `mvn clean package` must produce an executable jar file.
This can be done via maven plugins such as [shade](https://maven.apache.org/plugins/maven-shade-plugin) or [assembly](https://maven.apache.org/plugins/maven-assembly-plugin) plugin.

Following command line options must be supported. 

Option | Description
------------ | -------------
-n, --number | The number of entities to display. [default to 10]
-e, --entity | The name of the entity (e.g., hashtag or mention). [default to hashtag]
-r, --reverse | Reverse the comparison (e.g., display most infrequent entities).
-i, --ignore-case |	Fold upper case to lower case characters (e.g., collate #AnadoluÜniversitesi and #anadoluÜniversitesi).

The result will be printed to the standard output in the format of two columns (entity \t frequency) separated by a tab.

For example, `java jar target/nameOfTheExecutableJar -n 20 -e mention -i Tweets.txt` will display top-20 mentions ordered by their frequency.

P.S. To parse command line arguments, you can use [JewelCLI](http://jewelcli.lexicalscope.com) library.
Hint: [Regular Expressions](https://docs.oracle.com/javase/tutorial/essential/regex/) can be used for detecting entities.
