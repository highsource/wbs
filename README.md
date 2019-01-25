
How to use this example:

<pre>git clone https://github.com/obogrew/wbs.git

cd wbs

mvn clean
mvn generate-sources

ls src\main\generated\org
</pre>
-> package name is "<b>wrong</b>" It means that the mapping has not fired.

Let's remove the import and create one WSDL file instead of two. It is done on another branch.

<pre>
rm -rf src\main\generated

git checkout no_import

mvn clean
mvn generate-sources

ls src\main\generated\org
</pre>

-> package name is "<b>right</b>" The mapping has fired and namespace has changed from <i>org.wrong</i> to <i>org.right</i>
