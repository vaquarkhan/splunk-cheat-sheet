# Splunk-cheat-sheet

        index=<Your-Index-Name>_* cf_app_name=*<Appname>* <anysearch key>
        
         index="<index>_*" sourcetype="cf:logmessage" cf_app_name="<APP-NAME>*" cf_space_name="*" source_type="APP/PROC/WEB"   "msg.logLevel"=INFO "*<keyword for search>*"


![Alt Text](https://www.learnsplunk.com/uploads/2/7/1/9/2719363/7109108_orig.png)

*  Enter the keyword you want to search and click on  search example If you want to search for errors in your environment just type error in searchbox and hit enter Below is screenshot of sample results you get:

 
#### AND ,OR operator in splunk search

                        "error" AND  "databse" 
                        "error" or  "databse" 

#### Splunk Top command

                        error |  top limit=1 error
                        
#### wildcards in splunk search

                       keyword 2* it will shows all logs which contains 2 or 200 or 21,207 etc.
                       
#### dedup command

Dedup command removes duplicate values from the result.

                          * | dedup uid


 
#### head and tail 

If searched for all errors and pipe it to head it will display first 10 most recent logs for errors and vice versa for tail



                      error | head or error | head limit=10


#### stats 

Give you statics i.e number of occurrence of the event/Filed.

                      error |stats count by error


#### eval 

Eval modifies or creates new filed.Eval is  normally used to evaluate an arbitery expression,perform mathematical operations,renaming fields etc

-----------------------------------------------------------------------
#### Splunk Search book 

- http://docs.splunk.com/index.php?title=Documentation:Splunk:SearchReference:WhatsInThisManual:6.0beta&action=pdfbook


More refrences:

- http://docs.splunk.com/Documentation/Splunk/6.2.1/SearchReference/ListOfPopularSearchCommands
- http://docs.splunk.com/Documentation/Splunk/6.2.1/SearchReference/Commandsbycategory
- http://docs.splunk.com/Documentation/Splunk/6.2.1/SearchReference/SearchCheatsheet
- https://www.splunk.com/pdfs/solution-guides/splunk-quick-reference-guide.pdf
- https://wiki.splunk.com/images/2/2b/Cheatsheet.pdf
- http://www.innovato.com/splunk/RefCard.pdf
- https://mindmajix.com/splunk-regex-cheatsheet
- https://lzone.de/cheat-sheet/Splunk
- 
