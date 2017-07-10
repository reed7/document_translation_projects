





<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
  <link rel="dns-prefetch" href="https://assets-cdn.github.com">
  <link rel="dns-prefetch" href="https://avatars0.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars1.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars2.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars3.githubusercontent.com">
  <link rel="dns-prefetch" href="https://github-cloud.s3.amazonaws.com">
  <link rel="dns-prefetch" href="https://user-images.githubusercontent.com/">



  <link crossorigin="anonymous" href="https://assets-cdn.github.com/assets/frameworks-e04a23d39bf81b7db3c635177756ef51bc171feb440be9e174933c6eb56382da.css" integrity="sha256-4Eoj05v4G32zxjUXd1bvUbwXH+tEC+nhdJM8brVjgto=" media="all" rel="stylesheet" />
  <link crossorigin="anonymous" href="https://assets-cdn.github.com/assets/github-0eefc2e653e37f1e1077333bf8fa9ccdd7614e6f8ac38102f64367ab8165b029.css" integrity="sha256-Du/C5lPjfx4QdzM7+PqczddhTm+Kw4EC9kNnq4FlsCk=" media="all" rel="stylesheet" />
  
  
  
  

  <meta name="viewport" content="width=device-width">
  
  <title>spring-5-framework-doc/17_XML_Marshalling.md at master · lfvepclr/spring-5-framework-doc</title>
  <link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="GitHub">
  <link rel="fluid-icon" href="https://github.com/fluidicon.png" title="GitHub">
  <meta property="fb:app_id" content="1401488693436528">

    
    <meta content="https://avatars2.githubusercontent.com/u/4045814?v=3&amp;s=400" property="og:image" /><meta content="GitHub" property="og:site_name" /><meta content="object" property="og:type" /><meta content="lfvepclr/spring-5-framework-doc" property="og:title" /><meta content="https://github.com/lfvepclr/spring-5-framework-doc" property="og:url" /><meta content="spring-5-framework-doc - Spring 5 framework 翻译文档" property="og:description" />

  <link rel="assets" href="https://assets-cdn.github.com/">
  <link rel="web-socket" href="wss://live.github.com/_sockets/VjI6MTc0NDM0NDc2OjcwMWY0NDZiYTFlOWIyMWY0ZmZhOThiMDJiZjA1MGYyOGIxNjY3ZTk0MWZmNmVjYTI5MTY3MmExYjlmMTc0YWQ=--adb8c3ff4dca348b4701046e5c6a7c14e862b85a">
  <meta name="pjax-timeout" content="1000">
  <link rel="sudo-modal" href="/sessions/sudo_modal">
  <meta name="request-id" content="CB08:2E1CA:2FED669:4A08687:5963DA50" data-pjax-transient>
  

  <meta name="selected-link" value="repo_source" data-pjax-transient>

  <meta name="google-site-verification" content="KT5gs8h0wvaagLKAVWq8bbeNwnZZK1r1XQysX3xurLU">
<meta name="google-site-verification" content="ZzhVyEFwb7w3e0-uOTltm8Jsck2F5StVihD0exw2fsA">
    <meta name="google-analytics" content="UA-3769691-2">

<meta content="collector.githubapp.com" name="octolytics-host" /><meta content="github" name="octolytics-app-id" /><meta content="https://collector.githubapp.com/github-external/browser_event" name="octolytics-event-url" /><meta content="CB08:2E1CA:2FED669:4A08687:5963DA50" name="octolytics-dimension-request_id" /><meta content="sea" name="octolytics-dimension-region_edge" /><meta content="iad" name="octolytics-dimension-region_render" /><meta content="1271807" name="octolytics-actor-id" /><meta content="reed7" name="octolytics-actor-login" /><meta content="a64b129cc27a4d213d8c654016210f0563c68742b47e0849af031e36d1378c3b" name="octolytics-actor-hash" />
<meta content="/&lt;user-name&gt;/&lt;repo-name&gt;/blob/show" data-pjax-transient="true" name="analytics-location" />




  <meta class="js-ga-set" name="dimension1" content="Logged In">


  

      <meta name="hostname" content="github.com">
  <meta name="user-login" content="reed7">

      <meta name="expected-hostname" content="github.com">
    <meta name="js-proxy-site-detection-payload" content="M2IxNDcwZTA2ZjE3NGJmYTdlYjc2YTQzNmZlYTgxMWZlNDM5MmY5MjUwYWE3MmQ1Y2ViMzhhZjM1YWRjNDA5OXx7InJlbW90ZV9hZGRyZXNzIjoiMzguMTI3LjE3Ny42OCIsInJlcXVlc3RfaWQiOiJDQjA4OjJFMUNBOjJGRUQ2Njk6NEEwODY4Nzo1OTYzREE1MCIsInRpbWVzdGFtcCI6MTQ5OTcxNjE4MSwiaG9zdCI6ImdpdGh1Yi5jb20ifQ==">


  <meta name="html-safe-nonce" content="633cf59f51ffeace281cdc39490a68a7c34d98e3">

  <meta http-equiv="x-pjax-version" content="e0a09c603742d0bab53423f224a0284e">
  

      <link href="https://github.com/lfvepclr/spring-5-framework-doc/commits/master.atom" rel="alternate" title="Recent Commits to spring-5-framework-doc:master" type="application/atom+xml">

  <meta name="description" content="spring-5-framework-doc - Spring 5 framework 翻译文档">
  <meta name="go-import" content="github.com/lfvepclr/spring-5-framework-doc git https://github.com/lfvepclr/spring-5-framework-doc.git">

  <meta content="4045814" name="octolytics-dimension-user_id" /><meta content="lfvepclr" name="octolytics-dimension-user_login" /><meta content="94390120" name="octolytics-dimension-repository_id" /><meta content="lfvepclr/spring-5-framework-doc" name="octolytics-dimension-repository_nwo" /><meta content="true" name="octolytics-dimension-repository_public" /><meta content="false" name="octolytics-dimension-repository_is_fork" /><meta content="94390120" name="octolytics-dimension-repository_network_root_id" /><meta content="lfvepclr/spring-5-framework-doc" name="octolytics-dimension-repository_network_root_nwo" /><meta content="false" name="octolytics-dimension-repository_explore_github_marketplace_ci_cta_shown" />


    <link rel="canonical" href="https://github.com/lfvepclr/spring-5-framework-doc/blob/master/17_XML_Marshalling.md" data-pjax-transient>


  <meta name="browser-stats-url" content="https://api.github.com/_private/browser/stats">

  <meta name="browser-errors-url" content="https://api.github.com/_private/browser/errors">

  <link rel="mask-icon" href="https://assets-cdn.github.com/pinned-octocat.svg" color="#000000">
  <link rel="icon" type="image/x-icon" href="https://assets-cdn.github.com/favicon.ico">

<meta name="theme-color" content="#1e2327">


  <meta name="u2f-support" content="true">

  </head>

  <body class="logged-in env-production emoji-size-boost page-blob">
    



  <div class="position-relative js-header-wrapper ">
    <a href="#start-of-content" tabindex="1" class="bg-black text-white p-3 show-on-focus js-skip-to-content">Skip to content</a>
    <div id="js-pjax-loader-bar" class="pjax-loader-bar"><div class="progress"></div></div>

    
    
    



        
<div class="header" role="banner">
  <div class="container clearfix">
    <a class="header-logo-invertocat" href="https://github.com/" data-hotkey="g d" aria-label="Homepage" data-ga-click="Header, go to dashboard, icon:logo">
  <svg aria-hidden="true" class="octicon octicon-mark-github" height="32" version="1.1" viewBox="0 0 16 16" width="32"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
</a>


        <div class="header-search scoped-search site-scoped-search js-site-search" role="search">
  <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/lfvepclr/spring-5-framework-doc/search" class="js-site-search-form" data-scoped-search-url="/lfvepclr/spring-5-framework-doc/search" data-unscoped-search-url="/search" method="get"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /></div>
    <label class="form-control header-search-wrapper js-chromeless-input-container">
        <a href="/lfvepclr/spring-5-framework-doc/blob/master/17_XML_Marshalling.md" class="header-search-scope no-underline">This repository</a>
      <input type="text"
        class="form-control header-search-input js-site-search-focus js-site-search-field is-clearable"
        data-hotkey="s"
        name="q"
        value=""
        placeholder="Search"
        aria-label="Search this repository"
        data-unscoped-placeholder="Search GitHub"
        data-scoped-placeholder="Search"
        autocapitalize="off">
        <input type="hidden" class="js-site-search-type-field" name="type" >
    </label>
</form></div>


      <ul class="header-nav float-left" role="navigation">
        <li class="header-nav-item">
          <a href="/pulls" aria-label="Pull requests you created" class="js-selected-navigation-item header-nav-link" data-ga-click="Header, click, Nav menu - item:pulls context:user" data-hotkey="g p" data-selected-links="/pulls /pulls/assigned /pulls/mentioned /pulls">
            Pull requests
</a>        </li>
        <li class="header-nav-item">
          <a href="/issues" aria-label="Issues you created" class="js-selected-navigation-item header-nav-link" data-ga-click="Header, click, Nav menu - item:issues context:user" data-hotkey="g i" data-selected-links="/issues /issues/assigned /issues/mentioned /issues">
            Issues
</a>        </li>
            <li class="header-nav-item">
              <a href="/marketplace" class="js-selected-navigation-item header-nav-link" data-ga-click="Header, click, Nav menu - item:marketplace context:user" data-selected-links=" /marketplace">
                Marketplace
</a>            </li>
          <li class="header-nav-item">
            <a class="header-nav-link" href="https://gist.github.com/" data-ga-click="Header, go to gist, text:gist">Gist</a>
          </li>
      </ul>

    
<ul class="header-nav user-nav float-right" id="user-links">
  <li class="header-nav-item">
    
    <a href="/notifications" aria-label="You have no unread notifications" class="header-nav-link notification-indicator tooltipped tooltipped-s js-socket-channel js-notification-indicator " data-channel="notification-changed:1271807" data-ga-click="Header, go to notifications, icon:read" data-hotkey="g n">
        <span class="mail-status "></span>
        <svg aria-hidden="true" class="octicon octicon-bell float-left" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M14 12v1H0v-1l.73-.58c.77-.77.81-2.55 1.19-4.42C2.69 3.23 6 2 6 2c0-.55.45-1 1-1s1 .45 1 1c0 0 3.39 1.23 4.16 5 .38 1.88.42 3.66 1.19 4.42l.66.58H14zm-7 4c1.11 0 2-.89 2-2H5c0 1.11.89 2 2 2z"/></svg>
</a>
  </li>

  <li class="header-nav-item dropdown js-menu-container">
    <a class="header-nav-link tooltipped tooltipped-s js-menu-target" href="/new"
       aria-label="Create new…"
       aria-expanded="false"
       aria-haspopup="true"
       data-ga-click="Header, create new, icon:add">
      <svg aria-hidden="true" class="octicon octicon-plus float-left" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M12 9H7v5H5V9H0V7h5V2h2v5h5z"/></svg>
      <span class="dropdown-caret"></span>
    </a>

    <div class="dropdown-menu-content js-menu-content">
      <ul class="dropdown-menu dropdown-menu-sw">
        
<a class="dropdown-item" href="/new" data-ga-click="Header, create new repository">
  New repository
</a>

  <a class="dropdown-item" href="/new/import" data-ga-click="Header, import a repository">
    Import repository
  </a>

<a class="dropdown-item" href="https://gist.github.com/" data-ga-click="Header, create new gist">
  New gist
</a>

  <a class="dropdown-item" href="/organizations/new" data-ga-click="Header, create new organization">
    New organization
  </a>



  <div class="dropdown-divider"></div>
  <div class="dropdown-header">
    <span title="lfvepclr/spring-5-framework-doc">This repository</span>
  </div>
    <a class="dropdown-item" href="/lfvepclr/spring-5-framework-doc/issues/new" data-ga-click="Header, create new issue">
      New issue
    </a>

      </ul>
    </div>
  </li>

  <li class="header-nav-item dropdown js-menu-container">
    <a class="header-nav-link name tooltipped tooltipped-sw js-menu-target" href="/reed7"
       aria-label="View profile and more"
       aria-expanded="false"
       aria-haspopup="true"
       data-ga-click="Header, show menu, icon:avatar">
      <img alt="@reed7" class="avatar" src="https://avatars1.githubusercontent.com/u/1271807?v=3&amp;s=40" height="20" width="20">
      <span class="dropdown-caret"></span>
    </a>

    <div class="dropdown-menu-content js-menu-content">
      <div class="dropdown-menu dropdown-menu-sw">
        <div class="dropdown-header header-nav-current-user css-truncate">
          Signed in as <strong class="css-truncate-target">reed7</strong>
        </div>

        <div class="dropdown-divider"></div>

        <a class="dropdown-item" href="/reed7" data-ga-click="Header, go to profile, text:your profile">
          Your profile
        </a>
        <a class="dropdown-item" href="/reed7?tab=stars" data-ga-click="Header, go to starred repos, text:your stars">
          Your stars
        </a>
        <a class="dropdown-item" href="/explore" data-ga-click="Header, go to explore, text:explore">
          Explore
        </a>
        <a class="dropdown-item" href="https://help.github.com" data-ga-click="Header, go to help, text:help">
          Help
        </a>

        <div class="dropdown-divider"></div>

        <a class="dropdown-item" href="/settings/profile" data-ga-click="Header, go to settings, icon:settings">
          Settings
        </a>

        <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/logout" class="logout-form" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="TDKZtViio0z3ZIXTP4N093nTQyrZRmqZbLAl8tad3ngT0vvcRVi+sLRLhYAMcCKFpe+F54mQJ7z8E+Jx9EggLg==" /></div>
          <button type="submit" class="dropdown-item dropdown-signout" data-ga-click="Header, sign out, icon:logout">
            Sign out
          </button>
</form>      </div>
    </div>
  </li>
</ul>


    <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/logout" class="sr-only right-0" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="9VTEnbVMq1iJI8DKHtmNybhcIfv8BKOwOvI0xQAl5juqtKb0qLa2pMoMwJktKtu7ZGDnNqzS7pWqUfNGIvAYbQ==" /></div>
      <button type="submit" class="dropdown-item dropdown-signout" data-ga-click="Header, sign out, icon:logout">
        Sign out
      </button>
</form>  </div>
</div>


      

  </div>

  <div id="start-of-content" class="show-on-focus"></div>

    <div id="js-flash-container">
</div>



  <div role="main">
        <div itemscope itemtype="http://schema.org/SoftwareSourceCode">
    <div id="js-repo-pjax-container" data-pjax-container>
      




    <div class="pagehead repohead instapaper_ignore readability-menu experiment-repo-nav">
      <div class="container repohead-details-container">

        <ul class="pagehead-actions">
  <li>
        <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/notifications/subscribe" class="js-social-container" data-autosubmit="true" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="nDfCW/vMo7I06WGBPHZ6O0qO5apkrLj+lHkDLgOE3UwEkCpvl2WOps9Vtd1VTTbU9oRuJ4RwPdskC/b3oM/5YA==" /></div>      <input class="form-control" id="repository_id" name="repository_id" type="hidden" value="94390120" />

        <div class="select-menu js-menu-container js-select-menu">
          <a href="/lfvepclr/spring-5-framework-doc/subscription"
            class="btn btn-sm btn-with-count select-menu-button js-menu-target"
            role="button"
            aria-haspopup="true"
            aria-expanded="false"
            aria-label="Toggle repository notifications menu"
            data-ga-click="Repository, click Watch settings, action:blob#show">
            <span class="js-select-button">
                <svg aria-hidden="true" class="octicon octicon-eye" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                Unwatch
            </span>
          </a>
            <a class="social-count js-social-count"
              href="/lfvepclr/spring-5-framework-doc/watchers"
              aria-label="3 users are watching this repository">
              3
            </a>

        <div class="select-menu-modal-holder">
          <div class="select-menu-modal subscription-menu-modal js-menu-content">
            <div class="select-menu-header js-navigation-enable" tabindex="-1">
              <svg aria-label="Close" class="octicon octicon-x js-menu-close" height="16" role="img" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48z"/></svg>
              <span class="select-menu-title">Notifications</span>
            </div>

              <div class="select-menu-list js-navigation-container" role="menu">

                <div class="select-menu-item js-navigation-item " role="menuitem" tabindex="0">
                  <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"/></svg>
                  <div class="select-menu-item-text">
                    <input id="do_included" name="do" type="radio" value="included" />
                    <span class="select-menu-item-heading">Not watching</span>
                    <span class="description">Be notified when participating or @mentioned.</span>
                    <span class="js-select-button-text hidden-select-button-text">
                      <svg aria-hidden="true" class="octicon octicon-eye" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                      Watch
                    </span>
                  </div>
                </div>

                <div class="select-menu-item js-navigation-item selected" role="menuitem" tabindex="0">
                  <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"/></svg>
                  <div class="select-menu-item-text">
                    <input checked="checked" id="do_subscribed" name="do" type="radio" value="subscribed" />
                    <span class="select-menu-item-heading">Watching</span>
                    <span class="description">Be notified of all conversations.</span>
                    <span class="js-select-button-text hidden-select-button-text">
                      <svg aria-hidden="true" class="octicon octicon-eye" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                        Unwatch
                    </span>
                  </div>
                </div>

                <div class="select-menu-item js-navigation-item " role="menuitem" tabindex="0">
                  <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"/></svg>
                  <div class="select-menu-item-text">
                    <input id="do_ignore" name="do" type="radio" value="ignore" />
                    <span class="select-menu-item-heading">Ignoring</span>
                    <span class="description">Never be notified.</span>
                    <span class="js-select-button-text hidden-select-button-text">
                      <svg aria-hidden="true" class="octicon octicon-mute" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8 2.81v10.38c0 .67-.81 1-1.28.53L3 10H1c-.55 0-1-.45-1-1V7c0-.55.45-1 1-1h2l3.72-3.72C7.19 1.81 8 2.14 8 2.81zm7.53 3.22l-1.06-1.06-1.97 1.97-1.97-1.97-1.06 1.06L11.44 8 9.47 9.97l1.06 1.06 1.97-1.97 1.97 1.97 1.06-1.06L13.56 8l1.97-1.97z"/></svg>
                        Stop ignoring
                    </span>
                  </div>
                </div>

              </div>

            </div>
          </div>
        </div>
</form>
  </li>

  <li>
    
  <div class="js-toggler-container js-social-container starring-container ">
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/lfvepclr/spring-5-framework-doc/unstar" class="starred" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="uIAcMoJmLiPJdoomRT1cjCYsoPluJUgES+T1KEbh1nnleOBP1Lr+ljKXTlh5OqkrRBV2DADTLK7n0QaBPNYoAQ==" /></div>
      <button
        type="submit"
        class="btn btn-sm btn-with-count js-toggler-target"
        aria-label="Unstar this repository" title="Unstar lfvepclr/spring-5-framework-doc"
        data-ga-click="Repository, click unstar button, action:blob#show; text:Unstar">
        <svg aria-hidden="true" class="octicon octicon-star" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74z"/></svg>
        Unstar
      </button>
        <a class="social-count js-social-count" href="/lfvepclr/spring-5-framework-doc/stargazers"
           aria-label="6 users starred this repository">
          6
        </a>
</form>
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/lfvepclr/spring-5-framework-doc/star" class="unstarred" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="LfjFOkRhTFye6oTUvjH+VLMKiNeAiwVhCOFUYsq8sRbBsXESIZ252FWde48VvOcCC8POQD6EA+iXLIXQk3a1hQ==" /></div>
      <button
        type="submit"
        class="btn btn-sm btn-with-count js-toggler-target"
        aria-label="Star this repository" title="Star lfvepclr/spring-5-framework-doc"
        data-ga-click="Repository, click star button, action:blob#show; text:Star">
        <svg aria-hidden="true" class="octicon octicon-star" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74z"/></svg>
        Star
      </button>
        <a class="social-count js-social-count" href="/lfvepclr/spring-5-framework-doc/stargazers"
           aria-label="6 users starred this repository">
          6
        </a>
</form>  </div>

  </li>

  <li>
          <a href="#fork-destination-box" class="btn btn-sm btn-with-count"
              title="Fork your own copy of lfvepclr/spring-5-framework-doc to your account"
              aria-label="Fork your own copy of lfvepclr/spring-5-framework-doc to your account"
              rel="facebox"
              data-ga-click="Repository, show fork modal, action:blob#show; text:Fork">
              <svg aria-hidden="true" class="octicon octicon-repo-forked" height="16" version="1.1" viewBox="0 0 10 16" width="10"><path fill-rule="evenodd" d="M8 1a1.993 1.993 0 0 0-1 3.72V6L5 8 3 6V4.72A1.993 1.993 0 0 0 2 1a1.993 1.993 0 0 0-1 3.72V6.5l3 3v1.78A1.993 1.993 0 0 0 5 15a1.993 1.993 0 0 0 1-3.72V9.5l3-3V4.72A1.993 1.993 0 0 0 8 1zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3 10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3-10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
            Fork
          </a>

          <div id="fork-destination-box" style="display: none;">
            <h2 class="facebox-header" data-facebox-id="facebox-header">Where should we fork this repository?</h2>
            <include-fragment src=""
                class="js-fork-select-fragment fork-select-fragment"
                data-url="/lfvepclr/spring-5-framework-doc/fork?fragment=1">
              <img alt="Loading" height="64" src="https://assets-cdn.github.com/images/spinners/octocat-spinner-128.gif" width="64" />
            </include-fragment>
          </div>

    <a href="/lfvepclr/spring-5-framework-doc/network" class="social-count"
       aria-label="7 users forked this repository">
      7
    </a>
  </li>
</ul>

        <h1 class="public ">
  <svg aria-hidden="true" class="octicon octicon-repo" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
  <span class="author" itemprop="author"><a href="/lfvepclr" class="url fn" rel="author">lfvepclr</a></span><!--
--><span class="path-divider">/</span><!--
--><strong itemprop="name"><a href="/lfvepclr/spring-5-framework-doc" data-pjax="#js-repo-pjax-container">spring-5-framework-doc</a></strong>

</h1>

      </div>
      <div class="container">
        
<nav class="reponav js-repo-nav js-sidenav-container-pjax"
     itemscope
     itemtype="http://schema.org/BreadcrumbList"
     role="navigation"
     data-pjax="#js-repo-pjax-container">

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a href="/lfvepclr/spring-5-framework-doc" class="js-selected-navigation-item selected reponav-item" data-hotkey="g c" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches /lfvepclr/spring-5-framework-doc" itemprop="url">
      <svg aria-hidden="true" class="octicon octicon-code" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M9.5 3L8 4.5 11.5 8 8 11.5 9.5 13 14 8 9.5 3zm-5 0L0 8l4.5 5L6 11.5 2.5 8 6 4.5 4.5 3z"/></svg>
      <span itemprop="name">Code</span>
      <meta itemprop="position" content="1">
</a>  </span>

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a href="/lfvepclr/spring-5-framework-doc/issues" class="js-selected-navigation-item reponav-item" data-hotkey="g i" data-selected-links="repo_issues repo_labels repo_milestones /lfvepclr/spring-5-framework-doc/issues" itemprop="url">
        <svg aria-hidden="true" class="octicon octicon-issue-opened" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M7 2.3c3.14 0 5.7 2.56 5.7 5.7s-2.56 5.7-5.7 5.7A5.71 5.71 0 0 1 1.3 8c0-3.14 2.56-5.7 5.7-5.7zM7 1C3.14 1 0 4.14 0 8s3.14 7 7 7 7-3.14 7-7-3.14-7-7-7zm1 3H6v5h2V4zm0 6H6v2h2v-2z"/></svg>
        <span itemprop="name">Issues</span>
        <span class="Counter">0</span>
        <meta itemprop="position" content="2">
</a>    </span>

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a href="/lfvepclr/spring-5-framework-doc/pulls" class="js-selected-navigation-item reponav-item" data-hotkey="g p" data-selected-links="repo_pulls /lfvepclr/spring-5-framework-doc/pulls" itemprop="url">
      <svg aria-hidden="true" class="octicon octicon-git-pull-request" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M11 11.28V5c-.03-.78-.34-1.47-.94-2.06C9.46 2.35 8.78 2.03 8 2H7V0L4 3l3 3V4h1c.27.02.48.11.69.31.21.2.3.42.31.69v6.28A1.993 1.993 0 0 0 10 15a1.993 1.993 0 0 0 1-3.72zm-1 2.92c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zM4 3c0-1.11-.89-2-2-2a1.993 1.993 0 0 0-1 3.72v6.56A1.993 1.993 0 0 0 2 15a1.993 1.993 0 0 0 1-3.72V4.72c.59-.34 1-.98 1-1.72zm-.8 10c0 .66-.55 1.2-1.2 1.2-.65 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
      <span itemprop="name">Pull requests</span>
      <span class="Counter">0</span>
      <meta itemprop="position" content="3">
</a>  </span>

    <a href="/lfvepclr/spring-5-framework-doc/projects" class="js-selected-navigation-item reponav-item" data-selected-links="repo_projects new_repo_project repo_project /lfvepclr/spring-5-framework-doc/projects">
      <svg aria-hidden="true" class="octicon octicon-project" height="16" version="1.1" viewBox="0 0 15 16" width="15"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h13a1 1 0 0 0 1-1V1a1 1 0 0 0-1-1z"/></svg>
      Projects
      <span class="Counter" >0</span>
</a>
    <a href="/lfvepclr/spring-5-framework-doc/wiki" class="js-selected-navigation-item reponav-item" data-hotkey="g w" data-selected-links="repo_wiki /lfvepclr/spring-5-framework-doc/wiki">
      <svg aria-hidden="true" class="octicon octicon-book" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M3 5h4v1H3V5zm0 3h4V7H3v1zm0 2h4V9H3v1zm11-5h-4v1h4V5zm0 2h-4v1h4V7zm0 2h-4v1h4V9zm2-6v9c0 .55-.45 1-1 1H9.5l-1 1-1-1H2c-.55 0-1-.45-1-1V3c0-.55.45-1 1-1h5.5l1 1 1-1H15c.55 0 1 .45 1 1zm-8 .5L7.5 3H2v9h6V3.5zm7-.5H9.5l-.5.5V12h6V3z"/></svg>
      Wiki
</a>

    <div class="reponav-dropdown js-menu-container">
      <button type="button" class="btn-link reponav-item reponav-dropdown js-menu-target " data-no-toggle aria-expanded="false" aria-haspopup="true">
        Insights
        <svg aria-hidden="true" class="octicon octicon-triangle-down v-align-middle text-gray" height="11" version="1.1" viewBox="0 0 12 16" width="8"><path fill-rule="evenodd" d="M0 5l6 6 6-6z"/></svg>
      </button>
      <div class="dropdown-menu-content js-menu-content">
        <div class="dropdown-menu dropdown-menu-sw">
          <a class="dropdown-item" href="/lfvepclr/spring-5-framework-doc/pulse" data-skip-pjax>
            <svg aria-hidden="true" class="octicon octicon-pulse" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M11.5 8L8.8 5.4 6.6 8.5 5.5 1.6 2.38 8H0v2h3.6l.9-1.8.9 5.4L9 8.5l1.6 1.5H14V8z"/></svg>
            Pulse
          </a>
          <a class="dropdown-item" href="/lfvepclr/spring-5-framework-doc/graphs" data-skip-pjax>
            <svg aria-hidden="true" class="octicon octicon-graph" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M16 14v1H0V0h1v14h15zM5 13H3V8h2v5zm4 0H7V3h2v10zm4 0h-2V6h2v7z"/></svg>
            Graphs
          </a>
        </div>
      </div>
    </div>
</nav>

      </div>
    </div>

<div class="container new-discussion-timeline experiment-repo-nav">
  <div class="repository-content">

    
  <a href="/lfvepclr/spring-5-framework-doc/blob/06d1d5faf1799e487a58ad97436a6d59bee558e9/17_XML_Marshalling.md" class="d-none js-permalink-shortcut" data-hotkey="y">Permalink</a>

  <!-- blob contrib key: blob_contributors:v21:5c343e45e66cd536c38e7c694291a9ab -->

  <div class="file-navigation js-zeroclipboard-container">
    
<div class="select-menu branch-select-menu js-menu-container js-select-menu float-left">
  <button class=" btn btn-sm select-menu-button js-menu-target css-truncate" data-hotkey="w"
    
    type="button" aria-label="Switch branches or tags" aria-expanded="false" aria-haspopup="true">
      <i>Branch:</i>
      <span class="js-select-button css-truncate-target">master</span>
  </button>

  <div class="select-menu-modal-holder js-menu-content js-navigation-container" data-pjax>

    <div class="select-menu-modal">
      <div class="select-menu-header">
        <svg aria-label="Close" class="octicon octicon-x js-menu-close" height="16" role="img" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48z"/></svg>
        <span class="select-menu-title">Switch branches/tags</span>
      </div>

      <div class="select-menu-filters">
        <div class="select-menu-text-filter">
          <input type="text" aria-label="Filter branches/tags" id="context-commitish-filter-field" class="form-control js-filterable-field js-navigation-enable" placeholder="Filter branches/tags">
        </div>
        <div class="select-menu-tabs">
          <ul>
            <li class="select-menu-tab">
              <a href="#" data-tab-filter="branches" data-filter-placeholder="Filter branches/tags" class="js-select-menu-tab" role="tab">Branches</a>
            </li>
            <li class="select-menu-tab">
              <a href="#" data-tab-filter="tags" data-filter-placeholder="Find a tag…" class="js-select-menu-tab" role="tab">Tags</a>
            </li>
          </ul>
        </div>
      </div>

      <div class="select-menu-list select-menu-tab-bucket js-select-menu-tab-bucket" data-tab-filter="branches" role="menu">

        <div data-filterable-for="context-commitish-filter-field" data-filterable-type="substring">


            <a class="select-menu-item js-navigation-item js-navigation-open selected"
               href="/lfvepclr/spring-5-framework-doc/blob/master/17_XML_Marshalling.md"
               data-name="master"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"/></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                master
              </span>
            </a>
        </div>

          <div class="select-menu-no-results">Nothing to show</div>
      </div>

      <div class="select-menu-list select-menu-tab-bucket js-select-menu-tab-bucket" data-tab-filter="tags">
        <div data-filterable-for="context-commitish-filter-field" data-filterable-type="substring">


        </div>

        <div class="select-menu-no-results">Nothing to show</div>
      </div>

    </div>
  </div>
</div>

    <div class="BtnGroup float-right">
      <a href="/lfvepclr/spring-5-framework-doc/find/master"
            class="js-pjax-capture-input btn btn-sm BtnGroup-item"
            data-pjax
            data-hotkey="t">
        Find file
      </a>
      <button aria-label="Copy file path to clipboard" class="js-zeroclipboard btn btn-sm BtnGroup-item tooltipped tooltipped-s" data-copied-hint="Copied!" type="button">Copy path</button>
    </div>
    <div class="breadcrumb js-zeroclipboard-target">
      <span class="repo-root js-repo-root"><span class="js-path-segment"><a href="/lfvepclr/spring-5-framework-doc"><span>spring-5-framework-doc</span></a></span></span><span class="separator">/</span><strong class="final-path">17_XML_Marshalling.md</strong>
    </div>
  </div>


  
  <div class="commit-tease">
      <span class="float-right">
        <a class="commit-tease-sha" href="/lfvepclr/spring-5-framework-doc/commit/275727a0fc95f92a0121d2f7a154f43b8d6efce1" data-pjax>
          275727a
        </a>
        <relative-time datetime="2017-06-19T17:10:11Z">Jun 19, 2017</relative-time>
      </span>
      <div>
        <img alt="@reed7" class="avatar" height="20" src="https://avatars1.githubusercontent.com/u/1271807?v=3&amp;s=40" width="20" />
        <a href="/reed7" class="user-mention" rel="contributor">reed7</a>
          <a href="/lfvepclr/spring-5-framework-doc/commit/275727a0fc95f92a0121d2f7a154f43b8d6efce1" class="message" data-pjax="true" title="Update 17_XML_Marshalling.md">Update 17_XML_Marshalling.md</a>
      </div>

    <div class="commit-tease-contributors">
      <button type="button" class="btn-link muted-link contributors-toggle" data-facebox="#blob_contributors_box">
        <strong>1</strong>
         contributor
      </button>
      
    </div>

    <div id="blob_contributors_box" style="display:none">
      <h2 class="facebox-header" data-facebox-id="facebox-header">Users who have contributed to this file</h2>
      <ul class="facebox-user-list" data-facebox-id="facebox-description">
          <li class="facebox-user-list-item">
            <img alt="@reed7" height="24" src="https://avatars3.githubusercontent.com/u/1271807?v=3&amp;s=48" width="24" />
            <a href="/reed7">reed7</a>
          </li>
      </ul>
    </div>
  </div>

  <div class="file">
    <div class="file-header">
  <div class="file-actions">

    <div class="BtnGroup">
      <a href="/lfvepclr/spring-5-framework-doc/raw/master/17_XML_Marshalling.md" class="btn btn-sm BtnGroup-item" id="raw-url">Raw</a>
        <a href="/lfvepclr/spring-5-framework-doc/blame/master/17_XML_Marshalling.md" class="btn btn-sm js-update-url-with-hash BtnGroup-item" data-hotkey="b">Blame</a>
      <a href="/lfvepclr/spring-5-framework-doc/commits/master/17_XML_Marshalling.md" class="btn btn-sm BtnGroup-item" rel="nofollow">History</a>
    </div>

        <a class="btn-octicon tooltipped tooltipped-nw"
           href="https://desktop.github.com"
           aria-label="Open this file in GitHub Desktop"
           data-ga-click="Repository, open with desktop, type:mac">
            <svg aria-hidden="true" class="octicon octicon-device-desktop" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M15 2H1c-.55 0-1 .45-1 1v9c0 .55.45 1 1 1h5.34c-.25.61-.86 1.39-2.34 2h8c-1.48-.61-2.09-1.39-2.34-2H15c.55 0 1-.45 1-1V3c0-.55-.45-1-1-1zm0 9H1V3h14v8z"/></svg>
        </a>

        <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/lfvepclr/spring-5-framework-doc/edit/master/17_XML_Marshalling.md" class="inline-form js-update-url-with-hash" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="29hGA3faNExjRVMWdxwc0OaPcU+tL0EmDNdDRjtu7QcOqZTZBwO7bQV1yfEACtL+snAB9C53T/pP3tLZeTCS8Q==" /></div>
          <button class="btn-octicon tooltipped tooltipped-nw" type="submit"
            aria-label="Edit the file in your fork of this project" data-hotkey="e" data-disable-with>
            <svg aria-hidden="true" class="octicon octicon-pencil" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M0 12v3h3l8-8-3-3-8 8zm3 2H1v-2h1v1h1v1zm10.3-9.3L12 6 9 3l1.3-1.3a.996.996 0 0 1 1.41 0l1.59 1.59c.39.39.39 1.02 0 1.41z"/></svg>
          </button>
</form>        <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/lfvepclr/spring-5-framework-doc/delete/master/17_XML_Marshalling.md" class="inline-form" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="+fLlk3nlE7Vh7Ad1MMfMA8r+vbfbWY6Ye/RBjqZ+HkYi4Nq+FbYtZmyr5XQC+7/5o2Vtgl93ehQzMp+0Csd7Ng==" /></div>
          <button class="btn-octicon btn-octicon-danger tooltipped tooltipped-nw" type="submit"
            aria-label="Delete the file in your fork of this project" data-disable-with>
            <svg aria-hidden="true" class="octicon octicon-trashcan" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M11 2H9c0-.55-.45-1-1-1H5c-.55 0-1 .45-1 1H2c-.55 0-1 .45-1 1v1c0 .55.45 1 1 1v9c0 .55.45 1 1 1h7c.55 0 1-.45 1-1V5c.55 0 1-.45 1-1V3c0-.55-.45-1-1-1zm-1 12H3V5h1v8h1V5h1v8h1V5h1v8h1V5h1v9zm1-10H2V3h9v1z"/></svg>
          </button>
</form>  </div>

  <div class="file-info">
      357 lines (276 sloc)
      <span class="file-info-divider"></span>
    18.5 KB
  </div>
</div>

    
  <div id="readme" class="readme blob instapaper_body">
    <article class="markdown-body entry-content" itemprop="text"><h1><a id="user-content-17-使用-oxobjectxml映射器对xml进行编组" class="anchor" href="#17-使用-oxobjectxml映射器对xml进行编组" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17. 使用 O/X(Object/XML)映射器对XML进行编组</h1>
<h2><a id="user-content-171-简介" class="anchor" href="#171-简介" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.1 简介</h2>
<p>本章将讨论Spring对于 对象/XML 映射的支持。对象/XML 映射，或 O/X 映射，是指将 XML 文档与 XML 文档对象进行互相转换的操作。这一转换操作也被称作 XML 编组，或 XML 序列化。在本章中，这几个概念都指的是同一个东西。
在 O/X 映射中，将一组对象序列化为 XML 的操作是由一个编组器负责的。与之相对，一个反编组器则被用于将 XML 反序列化为一组对象。而这些操作中的 XML 文件来源可能是一份 DOM 文档，一个输入/输出流，或一个 SAX 管理器。
使用 Spring 提供的支持来实现你的 O/X 映射需求具有如下一些好处：</p>
<h3><a id="user-content-1711-便于配置" class="anchor" href="#1711-便于配置" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.1.1 便于配置</h3>
<p>Spring 的 bean 工厂使得无需构建 JAXB 上下文、JiBX 绑定工厂就可以配置编组器。你可以像配置你的应用中任何一个 Spring bean 一样地配置编组器。另外，相当一部分编组器可以使用基于 XML 架构的配置来进行设置，这让配置工作变得更为容易。</p>
<h3><a id="user-content-1712-一致的接口" class="anchor" href="#1712-一致的接口" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.1.2 一致的接口</h3>
<p>Spring 的 O/X 映射通过两个全局的接口来执行操作：Marshaller 和 Unmarshaller。这一结构让用户可以在几乎不需要修改编组操作类的前提下，轻易地在不同的 O/X 映射框架之间进行切换。这一结构的另一优势是可以以一种非侵入的方式在代码中混合多种 XML 编组方法（比如有一些编组实现使用 JAXB，而另一些则使用 Castor），从而将各种技术的优势在应用中加以综合利用。</p>
<h3><a id="user-content-1713-一致的异常继承" class="anchor" href="#1713-一致的异常继承" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.1.3 一致的异常继承</h3>
<p>Spring 对来自底层 O/X 映射工具的异常进行了转换，以 XmlMappingException 的形式使之成为 Spring 自身异常继承体系的一部分。这些 Spring 运行时异常将初始异常封装其中，因此所有异常信息都会被完整地保留下来。</p>
<h2><a id="user-content-172-编组器与反编组器" class="anchor" href="#172-编组器与反编组器" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.2 编组器与反编组器</h2>
<p>就如在“简介”中提到的，一个编组器负责将一个对象序列化成 XML，而一个反编组器则将 XML 流反序列化为一个对象。我们将在本节对 Spring 提供的两个相关接口进行描述。</p>
<h3><a id="user-content-1721-编组器" class="anchor" href="#1721-编组器" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.2.1 编组器</h3>
<p>Spring 将所有编组操作抽象成了 org.springframework.oxm.Marshaller 中的方法，以下是该接口最主要的一个方法：</p>
<pre><code>public interface Marshaller {
  /**
    * 将对象编组并存放在 Result 中.
    */
  void marshal(Object graph, Result result) throws XmlMappingException, IOException;
}
</code></pre>
<p>Marshaller 接口有一个主方法用于将一个给定对象编组为一个给定的 javax.xml.transform.Result 实现。这里的 Result 是一个用于代表某种 XML 输出格式的标记接口：不同的 Result 实现会封装不同的 XML 表现形式，详见下表：</p>
<table>
<thead>
<tr>
<th>Result 的实现</th>
<th>封装的 XML 表现形式</th>
</tr>
</thead>
<tbody>
<tr>
<td>DOMResult</td>
<td>org.w3c.dom.Node</td>
</tr>
<tr>
<td>SAXResult</td>
<td>org.xml.sax.ContentHandler</td>
</tr>
<tr>
<td>StreamResult</td>
<td>java.io.File, java.io.OutputStream, or java.io.Writer</td>
</tr></tbody></table>
<p>尽管 marshal() 方法的第一个参数只是一个简单对象，但大多数 Marshaller 实现并不真的能处理任意类型的对象。要么这个对象必须在映射文件中定义过映射关系，要么被注解所修饰，要么在编组器中进行过注册，要么与编组器实现拥有共同的基类。参考后面的章节来确定你所选用的 O/X 技术实现具体是怎么做的。</p>
<h3><a id="user-content-1722-反编组器" class="anchor" href="#1722-反编组器" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.2.2 反编组器</h3>
<p>与 Marshaller 接口相对应，还有一个 org.springframework.oxm.Unmarshaller 接口。</p>
<pre><code>public interface Unmarshaller {
   /**
     *  将来源 XML 反编组成一个对象
     */
   Object unmarshal(Source source) throws XmlMappingException, IOException;
}
</code></pre>
<p>此接口同样也有一个方法，从 javax.xml.transform.Source （一个抽象的 XML 输入）读取 XML 数据，并返回一个相对应的 Java 对象。和 Result 接口一样，Source 是一个拥有三个具体实现的标记接口。每一个实现封装了一种 XML 表现形式。详见下表：</p>
<table>
<thead>
<tr>
<th>Source 的实现</th>
<th>封装的 XML 表现形式</th>
</tr>
</thead>
<tbody>
<tr>
<td>DOMSource</td>
<td>org.w3c.dom.Node</td>
</tr>
<tr>
<td>SAXSource</td>
<td>org.xml.sax.InputSource, and org.xml.sax.XMLReader</td>
</tr>
<tr>
<td>StreamSource</td>
<td>java.io.File, java.io.OutputStream, or java.io.Writer</td>
</tr></tbody></table>
<h3><a id="user-content-1723-xmlmappingexception" class="anchor" href="#1723-xmlmappingexception" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.2.3 XmlMappingException</h3>
<p>Spring 对来自底层 O/X 映射工具的异常进行了转换，以 XmlMappingException 的形式使之成为 Spring 自身异常继承体系的一部分。 这些 Spring 运行时异常将初始异常封装其中，因此所有异常信息都会被完整地保留下来。
额外地，虽然底层的 O/X 映射工具并未提供支持，但 MarshallingFailureException 和 UnmarshallingFailureException 让编组与反编组操作中产生的异常得以能够被区分开来。
The O/X Mapping exception hierarchy is shown in the following figure:</p>
<p>以下是 O/X 映射异常的继承层次：</p>
<p><a href="https://camo.githubusercontent.com/8211719d377d042900750fec72cd2557585d35fd/68747470733a2f2f69322e77702e636f6d2f646f63732e737072696e672e696f2f737072696e672f646f63732f352e302e302e4d352f737072696e672d6672616d65776f726b2d7265666572656e63652f68746d6c2f696d616765732f6f786d2d657863657074696f6e732e706e672e7061676573706565642e63652e6d53374d786e716248362e706e67" target="_blank"><img src="https://camo.githubusercontent.com/8211719d377d042900750fec72cd2557585d35fd/68747470733a2f2f69322e77702e636f6d2f646f63732e737072696e672e696f2f737072696e672f646f63732f352e302e302e4d352f737072696e672d6672616d65776f726b2d7265666572656e63652f68746d6c2f696d616765732f6f786d2d657863657074696f6e732e706e672e7061676573706565642e63652e6d53374d786e716248362e706e67" alt="" data-canonical-src="https://i2.wp.com/docs.spring.io/spring/docs/5.0.0.M5/spring-framework-reference/html/images/oxm-exceptions.png.pagespeed.ce.mS7MxnqbH6.png" style="max-width:100%;"></a></p>
<h2><a id="user-content-173-marshaller-与-unmarshaller-的使用" class="anchor" href="#173-marshaller-与-unmarshaller-的使用" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.3 Marshaller 与 Unmarshaller 的使用</h2>
<p>Spring 的 OXM 可被用于十分广泛的场景。在以下的例子中，我们将使用这一功能将一个由 Spring 管理的应用程序的配置编组为一个 XML 文件。我们用了一个简单的 JavaBean 来表示这些配置：</p>
<pre><code>public class Settings {
	private boolean fooEnabled;
	public boolean isFooEnabled() {
		return fooEnabled;
	}
	public void setFooEnabled(boolean fooEnabled) {
		this.fooEnabled = fooEnabled;
	}
}
</code></pre>
<p>应用程序的主类使用这个 bean 来存放应用的配置信息。除了主要方法外，主类还包含下面两个方法：saveSettings() 将配置 bean 保存成一个名为 settings.xml 的文件， loadSettings() 则将配置信息从 XML 文件中读取出来。另有一个 main() 方法负责构建 Spring 应用上下文，并调用前述两个方法。</p>
<pre><code>import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;
import javax.xml.transform.stream.StreamResult;
import javax.xml.transform.stream.StreamSource;
import org.springframework.context.ApplicationContext;
import org.springframework.context.support.ClassPathXmlApplicationContext;
import org.springframework.oxm.Marshaller;
import org.springframework.oxm.Unmarshaller;
public class Application {
	private static final String FILE_NAME = "settings.xml";
	private Settings settings = new Settings();
	private Marshaller marshaller;
	private Unmarshaller unmarshaller;
	
	public void setMarshaller(Marshaller marshaller) {
		this.marshaller = marshaller;
	}
	
	public void setUnmarshaller(Unmarshaller unmarshaller) {
		this.unmarshaller = unmarshaller;
	}
	
	public void saveSettings() throws IOException {
		FileOutputStream os = null;
		try {
			os = new FileOutputStream(FILE_NAME);
			this.marshaller.marshal(settings, new StreamResult(os));
		} finally {
			if (os != null) {
				os.close();
			}
		}
	}
	
	public void loadSettings() throws IOException {
		FileInputStream is = null;
		try {
			is = new FileInputStream(FILE_NAME);
			this.settings = (Settings) this.unmarshaller.unmarshal(new StreamSource(is));
		} finally {
			if (is != null) {
				is.close();
			}
		}
	}
	
	public static void main(String[] args) throws IOException {
		ApplicationContext appContext =
				new ClassPathXmlApplicationContext("applicationContext.xml");
		Application application = (Application) appContext.getBean("application");
		application.saveSettings();
		application.loadSettings();
	}
}
</code></pre>
<p>需要将 marshaller 和 unmarshaller 这两个属性赋值才能使 Application 正确运行。我们可以使用以下 applicationContext.xml 的内容来实现这一目的：</p>
<pre><code>&lt;beans&gt;
	&lt;bean id="application" class="Application"&gt;
		&lt;property name="marshaller" ref="castorMarshaller" /&gt;
		&lt;property name="unmarshaller" ref="castorMarshaller" /&gt;
	&lt;/bean&gt;
	&lt;bean id="castorMarshaller" class="org.springframework.oxm.castor.CastorMarshaller"/&gt;
&lt;/beans&gt;
</code></pre>
<p>该应用中使用了 Castor 这一编组器实例，但我们可以使用在本章稍后描述的任何一个编组器实例来替换 Castor。Castor 默认并不需要任何进一步的配置，所以 bean 定义十分简洁。另外由于 CastorMarshaller 同时实现了 Marshaller 与 Unmarshaller 接口，所以我们可以同时把 castorMarshaller bean 赋值给应用的 marshaller 与 unmarshaller 属性。</p>
<p>此范例应用将会产生如下 settings.xml 文件：</p>
<pre><code>&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;settings foo-enabled="false"/&gt;
</code></pre>
<h2><a id="user-content-174-基于-xml-架构的配置" class="anchor" href="#174-基于-xml-架构的配置" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.4 基于 XML 架构的配置</h2>
<p>可以使用来自 OXM 命名空间的 XML 标签是对编组器的配置变得更简洁。要使用这些标签，请在 XML 文件开头引用恰当的 XML 架构。以下是一个引用 oxm 的示例，请注意粗体字部分：</p>
<pre><code>&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;beans xmlns="http://www.springframework.org/schema/beans"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xmlns:oxm="http://www.springframework.org/schema/oxm" 
	xsi:schemaLocation="http://www.springframework.org/schema/beans 
	http://www.springframework.org/schema/beans/spring-beans.xsd 
	http://www.springframework.org/schema/oxm 
	http://www.springframework.org/schema/oxm/spring-oxm.xsd"&gt;
</code></pre>
<p>目前可用的标签有以下这些：<br>
• <a href="http://docs.spring.io/spring/docs/5.0.0.BUILD-SNAPSHOT/spring-framework-reference/htmlsingle/#oxm-jaxb2-xsd">jaxb2-marshaller</a><br>
• <a href="http://docs.spring.io/spring/docs/5.0.0.BUILD-SNAPSHOT/spring-framework-reference/htmlsingle/#oxm-jibx-xsd">jibx-marshaller</a><br>
• <a href="http://docs.spring.io/spring/docs/5.0.0.BUILD-SNAPSHOT/spring-framework-reference/htmlsingle/#oxm-castor-xsd">castor-marshaller</a><br></p>
<p>每一个标签将会在接下来的章节中逐一介绍。下面是一个 JAXB2 的配置示例：</p>
<pre><code>&lt;oxm:jaxb2-marshaller id="marshaller" contextPath="org.springframework.ws.samples.airline.schema"/&gt;
</code></pre>
<h2><a id="user-content-175-jaxb" class="anchor" href="#175-jaxb" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.5 JAXB</h2>
<p>JAXB 绑定编译器将 W3C XML 架构实现为一到数个 Java 类，一个 jaxb.properties 文件，可能还会有数个资源文件。JAXB 同时还支持从被注解的 Java 类生成 XML 架构。</p>
<p>Spring 支持基于 17.2 Marshaller 和 Unmarshaller 所提到的 Marshaller 和 Unmarshaller 结构实现的 JAXB 2.0 API 编组策略。相应的类文件都定义在   org.springframework.oxm.jaxb 包下面。</p>
<h3><a id="user-content-1751-jaxb2marshaller" class="anchor" href="#1751-jaxb2marshaller" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.5.1 Jaxb2Marshaller</h3>
<p>Jaxb2Marshaller 类同时实现了 Marshaller 和 Unmarshaller 接口。这个类需要上下文路径以正常运作，你可以通过 contextPath 属性来设置。上下文路径是一组由冒号（：）分隔的 Java 包名。这些包下面包含了由 XML 架构所生成的对应 Java 类。另外你可以通过设置一个叫 classesToBeBound 的属性来配置一组可以被编组器支持的类。架构的验证则通过向 bean 中配置一到多个 XML 架构的 xsd 文件资源来实现。下面是一个 bean 的配置示例：</p>
<pre><code>&lt;beans&gt;
	&lt;bean id="jaxb2Marshaller" class="org.springframework.oxm.jaxb.Jaxb2Marshaller"&gt;
		&lt;property name="classesToBeBound"&gt;
			&lt;list&gt;
				&lt;value&gt;org.springframework.oxm.jaxb.Flight&lt;/value&gt;
				&lt;value&gt;org.springframework.oxm.jaxb.Flights&lt;/value&gt;
			&lt;/list&gt;
		&lt;/property&gt;
		&lt;property name="schema" value="classpath:org/springframework/oxm/schema.xsd"/&gt;
	&lt;/bean&gt;
...
&lt;/beans&gt;
</code></pre>
<h3><a id="user-content-1752-基于-xml-架构的配置" class="anchor" href="#1752-基于-xml-架构的配置" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.5.2 基于 XML 架构的配置</h3>
<p>Jaxb2-marshaller 标签 配置了一个 org.springframework.oxm.jaxb.Jaxb2Marshaller 实例。以下是一个配置实例：</p>
<pre><code>&lt;oxm:jaxb2-marshaller id="marshaller" contextPath="org.springframework.ws.samples.airline.schema"/&gt;
</code></pre>
<p>如果要配置需要被绑定的类，则可以使用 class-to-be-bound 子标签：</p>
<pre><code>&lt;oxm:jaxb2-marshaller id="marshaller"&gt;
	&lt;oxm:class-to-be-bound name="org.springframework.ws.samples.airline.schema.Airport"/&gt;
	&lt;oxm:class-to-be-bound name="org.springframework.ws.samples.airline.schema.Flight"/&gt;
	...
&lt;/oxm:jaxb2-marshaller&gt;
</code></pre>
<p>可用的标签属性如下表：</p>
<table>
<thead>
<tr>
<th>属性</th>
<th>描述</th>
<th>是否必需</th>
</tr>
</thead>
<tbody>
<tr>
<td>id</td>
<td>编组器的id</td>
<td>no</td>
</tr>
<tr>
<td>contextPath</td>
<td>JAXB上下文路径</td>
<td>no</td>
</tr></tbody></table>
<h2><a id="user-content-176-castor" class="anchor" href="#176-castor" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.6 Castor</h2>
<p>Castor XML 映射是一个开源的 XML 绑定框架。它允许使用者将包含在一个 Java 对象模型中的数据转换成 XML 文档，或者反之。Castor 默认并不需要额外的配置就可以使用。但如果使用者希望能够对框架行为拥有更多的控制，则可以通过在配置中引入一个映射文件来达到这一目的。</p>
<p>读者可以从 Castor 的项目主页上了解更多相关内容。Spring 对这一框架的集成代码都在 org.springframework.oxm.castor 包底下。</p>
<h3><a id="user-content-1761-castormarshaller" class="anchor" href="#1761-castormarshaller" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.6.1 CastorMarshaller</h3>
<p>与 JAXB 类似，CastorMarshaller 类同时实现了 Marshaller 和 Unmarshaller 接口。它可以通过以下配置来被引用：</p>
<pre><code>&lt;beans&gt;
	&lt;bean id="castorMarshaller" class="org.springframework.oxm.castor.CastorMarshaller" /&gt;
	...
&lt;/beans&gt;
</code></pre>
<h3><a id="user-content-1762-映射" class="anchor" href="#1762-映射" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.6.2 映射</h3>
<p>尽管 Castor 的默认编组行为基本能够适应大部分应用场景，有时候还是需要一些自定义的能力。这一需求可以通过使用一个 Castor 的映射文件来实现。更多信息请参考 Castor XML Mapping。</p>
<p>映射文件可以通过 mapppingLocation 属性进行设置，如下是一个配置了 classpath 资源的示例：</p>
<pre><code>&lt;beans&gt;
	&lt;bean id="castorMarshaller" class="org.springframework.oxm.castor.CastorMarshaller" &gt;
		&lt;property name="mappingLocation" value="classpath:mapping.xml" /&gt;
	&lt;/bean&gt;
&lt;/beans&gt;
</code></pre>
<h3><a id="user-content-1763-基于-xml-架构的配置" class="anchor" href="#1763-基于-xml-架构的配置" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.6.3 基于 XML 架构的配置</h3>
<p>一个 castor-marshaller 代表了一个 org.springframework.oxm.castor.CastorMarshaller 实例。示例如下：
&lt;oxm:castor-marshaller id="marshaller" mapping-location="classpath:org/springframework/oxm/castor/mapping.xml"/&gt;</p>
<p>编组器实例可以用两种方式进行配置，一种是（通过 mapping-location 属性）指定映射文件的位置
，另一种则是（通过 target-class 或 target-package 属性）指定包含有相应 XML 描述信息的 Java POJO。后一种方式一般会与通过 XML 架构自动生成 Java 代码的功能结合使用。</p>
<p>以下是可用的标签属性：</p>
<table>
<thead>
<tr>
<th>属性</th>
<th>描述</th>
<th>是否必需</th>
</tr>
</thead>
<tbody>
<tr>
<td>id</td>
<td>编组器的id</td>
<td>no</td>
</tr>
<tr>
<td>encoding</td>
<td>反编组 XML 文件使用的编码</td>
<td>no</td>
</tr>
<tr>
<td>target-class</td>
<td>一个 Java POJO 类名，此类中包含一个（由代码自动生成器生成的） XML 类的描述信息</td>
<td>no</td>
</tr>
<tr>
<td>target-package</td>
<td>一个包含了（由代码自动生成器生成的）POJO 和相应 Castor XML 描述类的 Java 包名</td>
<td>no</td>
</tr>
<tr>
<td>mapping-location</td>
<td>Castor XML 映射文件的位置</td>
<td>no</td>
</tr></tbody></table>
<h2><a id="user-content-177-jibx" class="anchor" href="#177-jibx" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.7 JiBX</h2>
<p>JiBX 框架提供的解决方案思路与 Hibernate 对于 ORM 的解决方案思路类似：通过一个绑定定义指定了你的 Java 对象与 XML 文件之间互相转换的规则。在准备好绑定并编译了类文件后，一个 JiBX 编译器将会对编译好的类文件进行增强，在其中加入一些辅助代码，并自动添加用于处理在类实例与 XML 文档之间相互转换的操作代码。</p>
<p>请参考 <a href="http://jibx.sourceforge.net/">JiBX官方网站</a> 来了解更多信息。Spring 对于框架的集成代码则都在 org.springframework.oxm.jibx 包下面。</p>
<h3><a id="user-content-1771-jibxmarshaller" class="anchor" href="#1771-jibxmarshaller" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.7.1 JibxMarshaller</h3>
<p>JiBXMarshaller 类同时实现了 Marshaller 和 Unmarshaller 接口。它需要使用者设置编组的目的类的类名才能正确工作。设置类名的属性是 targetClass。另外还有一个可选属性是 bingdingName，用户可以通过这个属性配置绑定名。接下来的示例中，我们将绑定 Flight 类：</p>
<pre><code>&lt;beans&gt;
	&lt;bean id="jibxFlightsMarshaller" class="org.springframework.oxm.jibx.JibxMarshaller"&gt;
		&lt;property name="targetClass"&gt;org.springframework.oxm.jibx.Flights&lt;/property&gt;
	&lt;/bean&gt;
	...
&lt;/beans&gt;
</code></pre>
<p>一个 JibxMarshaller 只能处理一个目的类与 XML 的相互转换，如果你需要编组多个类，你必需配置相应数量的 JibxMarshallers bean，然后在 targetClass 里面指定相应各个类的类名。</p>
<h3><a id="user-content-1772-基于-xml-的配置" class="anchor" href="#1772-基于-xml-的配置" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.7.2 基于 XML 的配置</h3>
<p>jibx-marshaller 标签配置了  org.springframework.oxm.jibx.JibxMarshaller 的实例。以下是一个示例：</p>
<pre><code>&lt;oxm:jibx-marshaller id="marshaller" target-class="org.springframework.ws.samples.airline.schema.Flight"/&gt;
</code></pre>
<p>标签的可用属性如下：</p>
<table>
<thead>
<tr>
<th>属性</th>
<th>描述</th>
<th>是否必需</th>
</tr>
</thead>
<tbody>
<tr>
<td>id</td>
<td>编组器的id</td>
<td>no</td>
</tr>
<tr>
<td>target-class</td>
<td>此编组器所对应的目标类</td>
<td>yes</td>
</tr>
<tr>
<td>bindingName</td>
<td>此编组器使用的绑定名</td>
<td>no</td>
</tr></tbody></table>
<h2><a id="user-content-178-xstream" class="anchor" href="#178-xstream" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>17.8 XStream</h2>
<p>Xstream 是一个用于将对象与 XML 文档进行序列化与反序列化的简单类库。它不需要任何映射关系，并且会生成整齐的 XML 文档。</p>
<p>请参考 <a href="https://x-stream.github.io/">XStream</a> 的项目主页以获取更多信息。Spring 对此框架的集成代码都在 org.springframework.oxm.xstream 包下面。</p>
<p>XstreamMarshaller 类不需进行任何配置便可直接在 applicationContext.xml 文件中直接配置成 bean 进行使用。不过你可以配置一个包含了字符串别名与类之间对应关系的 别名映射表  来实现对 XML 解析结果的自定义：</p>
<pre><code>&lt;beans&gt;
	&lt;bean id="xstreamMarshaller" class="org.springframework.oxm.xstream.XStreamMarshaller"&gt;
		&lt;property name="aliases"&gt;
			&lt;props&gt;
				&lt;prop key="Flight"&gt;org.springframework.oxm.xstream.Flight&lt;/prop&gt;
			&lt;/props&gt;
		&lt;/property&gt;
	&lt;/bean&gt;
	...
&lt;/beans&gt;
</code></pre>
<p><a href="https://camo.githubusercontent.com/1b63c1a0e03edc02fe21ec1e71199235d15f3b7f/687474703a2f2f646f63732e737072696e672e696f2f737072696e672f646f63732f352e302e302e4255494c442d534e415053484f542f737072696e672d6672616d65776f726b2d7265666572656e63652f68746d6c73696e676c652f696d616765732f7761726e696e672e706e672e7061676573706565642e63652e61473237527032624a592e706e67" target="_blank"><img src="https://camo.githubusercontent.com/1b63c1a0e03edc02fe21ec1e71199235d15f3b7f/687474703a2f2f646f63732e737072696e672e696f2f737072696e672f646f63732f352e302e302e4255494c442d534e415053484f542f737072696e672d6672616d65776f726b2d7265666572656e63652f68746d6c73696e676c652f696d616765732f7761726e696e672e706e672e7061676573706565642e63652e61473237527032624a592e706e67" alt="" data-canonical-src="http://docs.spring.io/spring/docs/5.0.0.BUILD-SNAPSHOT/spring-framework-reference/htmlsingle/images/warning.png.pagespeed.ce.aG27Rp2bJY.png" style="max-width:100%;"></a> Xstream 默认允许对任何类进行反编组操作，但这可能会导致安全隐患。因此不建议使用 XStreamMarshaller 对来源于外部（比如公网）的 XML 文档进行反编组。如果你坚持使用 XStreamMarshaller 反编组来自外部的 XML 文档，请如下例演示的一样设置 supportedClasses 属性：</p>
<pre><code>&lt;bean id="xstreamMarshaller" class="org.springframework.oxm.xstream.XStreamMarshaller"&gt;
	&lt;property name="supportedClasses" value="org.springframework.oxm.xstream.Flight"/&gt;
	...
&lt;/bean&gt;
</code></pre>
<p>设置这一属性能够确保只有指定的类才能够被用于反编组。</p>
<p>更进一步，你可以通过注册 <a href="http://docs.spring.io/spring-framework/docs/5.0.0.BUILD-SNAPSHOT/javadoc-api/org/springframework/oxm/xstream/XStreamMarshaller.html#setConverters(com.thoughtworks.xstream.converters.ConverterMatcher%E2%80%A6%E2%80%8B)">自定义转换器</a> 来确保只有你指定的类才能够被反编组。建议在明确指定了所有转换器后，在列表的最后加上 CatchAllConverter ，这样一来便可确保具有低优先级以及安全风险的 Xstream 默认转换器不会被调用。</p>
<p><a href="https://camo.githubusercontent.com/5f7ff0ff848e2d851bb8738cb2987fc3edfa5f01/687474703a2f2f646f63732e737072696e672e696f2f737072696e672f646f63732f352e302e302e4255494c442d534e415053484f542f737072696e672d6672616d65776f726b2d7265666572656e63652f68746d6c73696e676c652f696d616765732f6e6f74652e706e672e7061676573706565642e63652e397a515f317756777a522e706e67" target="_blank"><img src="https://camo.githubusercontent.com/5f7ff0ff848e2d851bb8738cb2987fc3edfa5f01/687474703a2f2f646f63732e737072696e672e696f2f737072696e672f646f63732f352e302e302e4255494c442d534e415053484f542f737072696e672d6672616d65776f726b2d7265666572656e63652f68746d6c73696e676c652f696d616765732f6e6f74652e706e672e7061676573706565642e63652e397a515f317756777a522e706e67" alt="" data-canonical-src="http://docs.spring.io/spring/docs/5.0.0.BUILD-SNAPSHOT/spring-framework-reference/htmlsingle/images/note.png.pagespeed.ce.9zQ_1wVwzR.png" style="max-width:100%;"></a> 这里需要注意的是 XStream 是一个 XML 序列化类库，而非一个数据绑定类库，所以它对命名空间的支持有限。这就使得 XStream 并不适合于用在网络服务中。</p>
</article>
  </div>

  </div>

  <button type="button" data-facebox="#jump-to-line" data-facebox-class="linejump" data-hotkey="l" class="d-none">Jump to Line</button>
  <div id="jump-to-line" style="display:none">
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="" class="js-jump-to-line-form" method="get"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /></div>
      <input class="form-control linejump-input js-jump-to-line-field" type="text" placeholder="Jump to line&hellip;" aria-label="Jump to line" autofocus>
      <button type="submit" class="btn">Go</button>
</form>  </div>

  </div>
  <div class="modal-backdrop js-touch-events"></div>
</div>

    </div>
  </div>

  </div>

      
<div class="container site-footer-container">
  <div class="site-footer " role="contentinfo">
    <ul class="site-footer-links float-right">
        <li><a href="https://github.com/contact" data-ga-click="Footer, go to contact, text:contact">Contact GitHub</a></li>
      <li><a href="https://developer.github.com" data-ga-click="Footer, go to api, text:api">API</a></li>
      <li><a href="https://training.github.com" data-ga-click="Footer, go to training, text:training">Training</a></li>
      <li><a href="https://shop.github.com" data-ga-click="Footer, go to shop, text:shop">Shop</a></li>
        <li><a href="https://github.com/blog" data-ga-click="Footer, go to blog, text:blog">Blog</a></li>
        <li><a href="https://github.com/about" data-ga-click="Footer, go to about, text:about">About</a></li>

    </ul>

    <a href="https://github.com" aria-label="Homepage" class="site-footer-mark" title="GitHub">
      <svg aria-hidden="true" class="octicon octicon-mark-github" height="24" version="1.1" viewBox="0 0 16 16" width="24"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
</a>
    <ul class="site-footer-links">
      <li>&copy; 2017 <span title="0.17454s from unicorn-3323094743-526rl">GitHub</span>, Inc.</li>
        <li><a href="https://github.com/site/terms" data-ga-click="Footer, go to terms, text:terms">Terms</a></li>
        <li><a href="https://github.com/site/privacy" data-ga-click="Footer, go to privacy, text:privacy">Privacy</a></li>
        <li><a href="https://github.com/security" data-ga-click="Footer, go to security, text:security">Security</a></li>
        <li><a href="https://status.github.com/" data-ga-click="Footer, go to status, text:status">Status</a></li>
        <li><a href="https://help.github.com" data-ga-click="Footer, go to help, text:help">Help</a></li>
    </ul>
  </div>
</div>



  <div id="ajax-error-message" class="ajax-error-message flash flash-error">
    <svg aria-hidden="true" class="octicon octicon-alert" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8.865 1.52c-.18-.31-.51-.5-.87-.5s-.69.19-.87.5L.275 13.5c-.18.31-.18.69 0 1 .19.31.52.5.87.5h13.7c.36 0 .69-.19.86-.5.17-.31.18-.69.01-1L8.865 1.52zM8.995 13h-2v-2h2v2zm0-3h-2V6h2v4z"/></svg>
    <button type="button" class="flash-close js-flash-close js-ajax-error-dismiss" aria-label="Dismiss error">
      <svg aria-hidden="true" class="octicon octicon-x" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48z"/></svg>
    </button>
    You can't perform that action at this time.
  </div>


    
    <script crossorigin="anonymous" integrity="sha256-ppOnsBnDIasqNFKIsGSIce0coP+bwNb7uTuu6vc2HpU=" src="https://assets-cdn.github.com/assets/frameworks-a693a7b019c321ab2a345288b0648871ed1ca0ff9bc0d6fbb93baeeaf7361e95.js"></script>
    
    <script async="async" crossorigin="anonymous" integrity="sha256-Fffm8UUiU0VdZ/lnBGGoZSdVj53P6KmILitBmA6O+L4=" src="https://assets-cdn.github.com/assets/github-15f7e6f1452253455d67f9670461a86527558f9dcfe8a9882e2b41980e8ef8be.js"></script>
    
    
    
    
  <div class="js-stale-session-flash stale-session-flash flash flash-warn flash-banner d-none">
    <svg aria-hidden="true" class="octicon octicon-alert" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8.865 1.52c-.18-.31-.51-.5-.87-.5s-.69.19-.87.5L.275 13.5c-.18.31-.18.69 0 1 .19.31.52.5.87.5h13.7c.36 0 .69-.19.86-.5.17-.31.18-.69.01-1L8.865 1.52zM8.995 13h-2v-2h2v2zm0-3h-2V6h2v4z"/></svg>
    <span class="signed-in-tab-flash">You signed in with another tab or window. <a href="">Reload</a> to refresh your session.</span>
    <span class="signed-out-tab-flash">You signed out in another tab or window. <a href="">Reload</a> to refresh your session.</span>
  </div>
  <div class="facebox" id="facebox" style="display:none;">
  <div class="facebox-popup">
    <div class="facebox-content" role="dialog" aria-labelledby="facebox-header" aria-describedby="facebox-description">
    </div>
    <button type="button" class="facebox-close js-facebox-close" aria-label="Close modal">
      <svg aria-hidden="true" class="octicon octicon-x" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48z"/></svg>
    </button>
  </div>
</div>


  </body>
</html>

