0.0.9
-------

Now allows clients to have a say if a download should go ahead or not. See #29 You hook into this through your Application class.

0.0.8
-------

Enforces passing a Context via the DownloadManagerBuilder this allows Requests created later on to not need to pass Context as a parameter. (#28)
It will also allow us to make further refactorings behind the scenes now we haz your Context bwahaha.
THIS IS AN API BREAKING CHANGE FOR DownloadManagerBuilder, DownloadManager and Request (see https://thechive.files.wordpress.com/2013/01/gifs_201.gif)

0.0.7
-------

Adds the ability to configure the maximum concurrent downloads (see #23)
Improves performance of notification image fetching (#27)

0.0.6
-------

PERFORMANCE FIX - removes verbose logging by default, this stops extra queries and string concat's that caused unneccessary GC
You can now set verbose logging on using the new `DownloadManagerBuilder.withVerboseLogging()` it is off by default. (see #20)

0.0.5
-------

Removes unused constants & minimises our public API, now we can refactor internally more safely

0.0.4
-------

Prefixes all resources with `dl__` , fixes but where the `app_name` for some clients would be "DownloadManager"

0.0.3
-------

Exposes the `DownloadManager.CONTENT_URI` so clients can query however they want (for example Loaders)

0.0.2
-------

Allows selection of content provider authority using `manifestPlaceholders = [downloadAuthority: "${applicationId}"]` and class `com.novoda.downloadmanager.Authority`

0.0.1
-------

Initial release - do not use - you will have issues with conflicting content providers if you use in more than one app (and anyone elses apps)
