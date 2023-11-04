# Notes

1. Use cURL to obtain the source code of the “https://www.inlanefreight.com” website and filter all unique paths of that domain. 
    - [Link](https://forum.hackthebox.com/t/use-curl-from-your-pwnbox-not-the-target-machine-to-obtain-the-source-code-of-the-https-www-inlanefreight-com-website-and-filter-all-unique-paths-of-that-domain-submit-the-number-of-these-paths-as-the-answer/260723/1)
    - `curl https://www.inlanefreight.com >> inlanefreight.txt`
    - `cat inlanefreight.txt |grep -Po "https://www.inlanefreight.com/[^'\"]*" | sort -u`
    - this one also works
    - `cat inlanefreight.txt |tr " " "\n" |cut -d "'" -f2 |cut -d '"' -f2 |grep "www.   inlanefreight.com/" |sort -u`

    ```
    https://www.inlanefreight.com/
    https://www.inlanefreight.com/index.php/about-us/
    https://www.inlanefreight.com/index.php/career/
    https://www.inlanefreight.com/index.php/comments/feed/
    https://www.inlanefreight.com/index.php/contact/
    https://www.inlanefreight.com/index.php/feed/
    https://www.inlanefreight.com/index.php/news/
    https://www.inlanefreight.com/index.php/offices/
    https://www.inlanefreight.com/index.php/wp-json/
    https://www.inlanefreight.com/index.php/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fwww. inlanefreight.com%2F
    https://www.inlanefreight.com/index.php/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fwww. inlanefreight.com%2F&#038;format=xml
    https://www.inlanefreight.com/index.php/wp-json/wp/v2/pages/7
    https://www.inlanefreight.com/wp-content/themes/ben_theme/css/animate.css?ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/css/bootstrap.css?ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/css/bootstrap-progressbar.min.css?    ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/css/colors/default.css?ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/css/font-awesome.css?ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/css/jquery.smartmenus.bootstrap.css?  ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/css/magnific-popup.css?ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/css/owl.carousel.css?ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/css/owl.transitions.css?ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/images/breadcrumb-back.jpg
    https://www.inlanefreight.com/wp-content/themes/ben_theme/js/bootstrap.min.js?ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/js/jquery.smartmenus.bootstrap.js?    ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/js/jquery.smartmenus.js?ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/js/navigation.js?ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/js/owl.carousel.min.js?ver=5.6.12
    https://www.inlanefreight.com/wp-content/themes/ben_theme/style.css?ver=5.6.12
    https://www.inlanefreight.com/wp-includes/css/dist/block-library/style.min.css?ver=5.6.12
    https://www.inlanefreight.com/wp-includes/js/jquery/jquery-migrate.min.js?ver=3.3.2
    https://www.inlanefreight.com/wp-includes/js/jquery/jquery.min.js?ver=3.5.1
    https://www.inlanefreight.com/wp-includes/js/wp-embed.min.js?ver=5.6.12
    https://www.inlanefreight.com/wp-includes/wlwmanifest.xml
    https://www.inlanefreight.com/xmlrpc.php?rsd
    ```

2. 