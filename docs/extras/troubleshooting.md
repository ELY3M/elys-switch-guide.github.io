# Troubleshooting 
This page is about common issues with atmosphere and situations to fix them.   

   
   
   



# archive bits
None of my homebrew is showing up.  
atmosphere crash on boot with 
<pre>
A fatal error occurred when running Atmosphére.
Title ID: 010041544d530000
Error Desc: std::abort() called (0xffe)
</pre>   

This is usually due to an archive metadata bit used by some OS’s that Horizon simply can’t deal with. Here’s how to fix it:

1. Get your switch in RCM mode.  
2. Inject Hekate payload 
3. Tap on "Tools" on top of the hekate screen.  
4. Tap on "Archive Bit - AutoRCM" on the right bottom.  
5. Tap on "Unset archive bit" button.  This might take a while, be patient.


	   
&nbsp;
