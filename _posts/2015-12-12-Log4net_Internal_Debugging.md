---
title: "Log4net Internal Debugging"
tags: [log4net,c#,.net]
---

Log4net fails silently to prevent it from affecting the application. 
Internal logging can be turned on by adding the below config to the applications app.config.
<br/><br/>


{% highlight xml %} 

<?xml version="1.0" encoding="utf-8" ?>
<configuration>
    
	<!-- Other config for the application -->
	
	<appSettings>
		<!-- Other app settings for the application -->
        <add key="log4net.Internal.Debug" value="true"/> <!-- Turn on internal debugging -->
    </appSettings>
	
    <!-- Output diagnostics to the file C:\tmp\log4net.txt -->
    <system.diagnostics>
        <trace autoflush="true">
            <listeners>
                <add 
                    name="textWriterTraceListener" 
                    type="System.Diagnostics.TextWriterTraceListener" 
                    initializeData="C:\tmp\log4net.txt" />
            </listeners>
        </trace>
    </system.diagnostics>

</configuration>
{% endhighlight %}

Note: For some reason I had to add this at the bottom of the app.config after all of the other 
config parameters or the application failed to start.
<br/><br/>
More details on the <a href="https://logging.apache.org/log4net/release/faq.html">log4net FAQ</a> page under the heading <i>"How do I enable log4net internal debugging?"</i>



