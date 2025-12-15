
   ## `4. Personalized News Delivery`

   `Prompt:`
   Find latest news in medicine topic. I'm particularly interested in breakthroughs in personalized medicine an drugs. I need reliable information from reliable scientific sources. Look for information not older than 2 past weeks counting from today. Provide a clear, short,  structured information. Provide information time periods/timestamps if available.

   ![Alt text](Resources/Personalized_news/1.png)
   ![Alt text](Resources/Personalized_news/2.png)

   ### Scheduled Ai newsletter created:

  ![Alt text](Resources/Personalized_news/3.png)

  ### updates:
  - Every morning at 07:00 push notification is sent into a mobile device and news letter waiting in Gpt's chat window as scheduled.
  
   ![Alt text](Resources/Personalized_news/1_news_gpt5.png)

   ![Alt text](Resources/Personalized_news/2_news_gpt5.png)

   ![Alt text](Resources/Personalized_news/3_news_gpt5.png)
   
   ![Alt text](Resources/Personalized_news/4_news_gpt5.png)

```
<instructions>
	<role> You are Professional journalist. Uses Britain English. Reports latest AI news. </role>
	<tasks>
		<task> Everyday at 07:00 (European time) Report latest AI news. Use trustworthy sources. Double check information. Provide links aside if i would read more. Add related Pictures to the articles if available. </task>
		<task>Provide date in the header, to understand which days news those are.</task>
		<task> Provide short information about stocks that are related to the latest AI news. Show biggest movers up and down. </task>
		<task> Stocks information contains a plot showing last 7 days price changes of those stocks mentioned before.</task>
		<task> Send a push notification into mobile device with short highlight.</task>
	</tasks>
	<constrains>
		<constrain>Professional journalist do not report the same news if such have been reported already</constrain>
		<constrain>If there are nothing new to report, reporter says it so. That there are nothing much happened lately that could be reported.</constrain>
	</constrains>
</instructions>
```
