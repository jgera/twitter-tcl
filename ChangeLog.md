# twitter.tcl

## 0.3 - Unreleased
  - fix direct msg
  - replace decode_html with htmlparse::mapEscapes (though this isn't even
    really needed i think!)
  - add search users (!twit_searchusers)
  - fix home timeline to use GET rather than POST. thanks to demonicpagan!
  - change GETs that have http query to process params better
  - add !update_interval to change delay between tweet/timeline fetches
  - change specification of update interval in config slightly so that bind
    times are not needed to be manually edited
  - change flags for binds to requiring +o by default
  - remove output_channel variable in favour of output status updates to
    every channel that is set +twitter
  - add config option to not show tweetid
  - change output format
  - change default state_file filename & variable
  - require consumer key/secret specified in !twit_request_token rather than
    hardcode into oauth.tcl
  - fix failed tweet msg to make more sense (not assume http error)

## 0.2 - May 18 2010
  - add timeout to query to avoid hangs
  - update decode_html for more accurate utf translation
  - replace basic auth with oauth
  - misc cleanup/small bugfixes
  - add max_updates variable to control the number of status to display from
    one query

## 0.1 - Feb 6 2010
  - initial release


# oauth.tcl

## 0.2 - Unreleased
  - create base_url correctly for signing (remove ?params=...)
  - improve error msg if http timeout occurs
  - remove need to hardcode consumer key/secret by providing them as arguments
    to the various functions

# 0.1 - May 18 2010
  - Initial release
