Drupal Website Launch Checklist
=======================

- Perform load testing & optimization beforehand include slow-log analyses;
- Check Drupal SEO Tools report;
- Match recommendations of the following:
	- [Security Review Module](https://drupal.org/project/security_review);
    - [Site Audit module](https://drupal.org/project/site_audit);
    - Acquia Insight;
    - YSlow;
- Performance and Scalability Checklist module;
- Match the requirements of Acquia Insight;
- Analyze Coder Review results;
- Perform load testing using tools with cleared database cache, memcache and image styles when caches are disabled;
- Make sure you have a failover scenario and a quick backup;
- Configure Cron jobs;
- Disable all development modules;
- Add console.log stub;
- Configure caches properly: Varnish, Memcache;
- Check if CDNs are configured correctly for live environment;
- Make sure AJAX requests are cached;
- Enable bandwidth optimization;
    - Compress cached pages;
    - Aggregate and compress JS/CSS files;
        - Use [Advanced CSS/JS Aggregation](https://drupal.org/project/advagg) module instead of core aggregation;
- Test simultaneous an consequent anonymous access scenarios and behavior when every cache is enabled;
- Replace database logging functionality with other solutions, e.g. syslog;
- Disable any errors output on frontend;
- Enable fast_404 in settings.php file;
- [Make sure file permissions for file directories and code directory are set correctly](http://drupal.org/node/244924);
- Make sure that input formats are correctly configured;
- On /admin/config/system/site-information make sure the email address and name are correct;
- Ensure website permissions are set appropriately and minimally;
- Get rid of CHANGELOG.txt etc (from git etc). Do NOT remove robots.txt;
- If using SSL, change your local /etc/hosts to point the site to its live domain and ensure SSL redirection is working correctly;
- Remove test content, such as "lorum ipsum" text, dummy users, or content generated by the Devel module;
- Check the maximum file upload sizes and maximum execution time;
- If you don't use core Search module, make sure it's disabled;
- If you use any replacements for standard Cron, make sure it's disabled;
- Warm caches before launch:
    - Use [Cache Warmer module](https://drupal.org/project/cache_warmer);
    - Use [HTTPRL Spider module](https://drupal.org/project/httprl_spider);
- If possible, perform launch component-by-component and one-by-one.
