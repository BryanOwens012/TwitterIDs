# TwitterIDs

The program `TwitterConsole.exe` downloads the IDs of the followers of a certain Twitter user.

Thanks to **Bovey Qin**, who wrote the entire thing!

Here is his README:
———————————————————————————

Unzip the zip file to an folder, which we refer as unzipped folder.

The application is TwitterConsole.exe, a windows console application to get followers ids for a given screen name.

Usage:
TwitterConsole.exe [screenName]
For example:

TwitterConsole.exe billclinton

What does the above command do :

1. find billclinton's followerID, and save to a ID txt file in format of billclinton-followers-ids-635763954267209817.txt
the number part is system clock ticks and can be different in each run.
2. create a cursor file in name of billclinton_cursor, no file extension and the content is the last processed cursor.


Whenever the application runs, it will try to read saved cursor, and starts from this one.  That is a feature to 
make the application  resumable. It  will never start from the firt one, but always pick up the last operation and 
contiue. It makes possible to get all followers  in an increamental maner.

When this applicaiton runs for the same screen name multi-times, you need to combine all  different ID file. 

For example, we have run 3 time for billclinton and we got 3 ID file like below:
billclinton-followers-ids-635763954267209817.txt
billclinton-followers-ids-635763955428943858.txt
billclinton-followers-ids-635763957891564183.txt

Combine all above 3 file to get all follower's ID

Configuration.

There is a file called TwitterConsole.exe.config
The only thing interesting is the following section
<:appSettings>:
    <:add key="key1" value="o2tUMOkODE9hA5kvjjANZfUMq|NQAJiCJKtIAHHh1sB6SfoLnmXCnU6y0aBkxf9ShRyGz3J9os3e|3421384840-nMXEvElKMkJzdRMz6wc6WlkkaApmxGXRyy5VdVs|cMV6Ep7YyvX8sRJErJRECXluWvUBnd5MPrLJun4OiFP1a" />:
    <:add key="key2" value="RW1cM5XZxcYOxX6jfwvyiaQ5f|tMPSwTm8Nt2xORlJMhWpHOS6kuwykBAscJjuaPrMfOyuAhJox5|3421384840-6iMukx2bVGLrSbI2I5Z6pq6Yl6I8CUBXyugx4fo|Ssob8xneLwimSlRnNwSxHXAessidZtGr1qAYWJ67bhbNj" />:
    <:add key="key3" value="RW1cM5XZxcYOxX6jfwvyiaQ5f|tMPSwTm8Nt2xORlJMhWpHOS6kuwykBAscJjuaPrMfOyuAhJox5|3421384840-6iMukx2bVGLrSbI2I5Z6pq6Yl6I8CUBXyugx4fo|Ssob8xneLwimSlRnNwSxHXAessidZtGr1qAYWJ67bhbNj" />:
    <:add key="key4" value="vispVHANmFSw1yBjE4X87tZJg|QhTXU496wbn340FGWAnHQOdmChjAlqSnICmItBnhoyoebGyc1A|3421384840-ea70MplzaSuYX56fKLtmHdWJkaC1wVpFM6yvtRA|9uRU4TfgpwkR82fhQs7M5XX9p1Lwwd70ujUR8aGcFAJ5y" />:
  <:/appSettings>:

Each key is an Twitter API App. It is extendable.
If you need add another key,
 add key5, key6,key7 etc.


Most powerful feature:

You can run the application to different screen name in the same time.

Open command line windows and navigate to the unzipped folder and run
TwitterConsole.exe hillaryclinton


then open another command line windows and navigate to the unzipped folder and run it again to target another people:
TwitterConsole.exe joebidden

you can repeat above step to start working on mulit people.

My test is to work on 6 people for about 2 or 3 hours and get more than 2 million ids.

all joebidden's followers is done. Don't run him again.
When one's followers is fetched completely, there will some showing like
All followers fetched. No more followers
then you can close this window.


In the zip file there are 6 cursor files, that meand I have started to work on 6 persons, but only joebidden is done.

Other 5 persons is not complete. if you start run this applicaiton on any one of the remaining 5, you will
continue from where I left.

You need to divid persons among you 2. You can run the same person in different time at the same machine, but not 
the same time at different machine. One person has to stick to one machine. If you need to change person please share 
cursor file.
