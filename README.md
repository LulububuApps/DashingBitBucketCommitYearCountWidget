## Description

Simple [Dashing](http://shopify.github.com/dashing) job to display the commit counts of a specific year of all [Bitbucket](https://bitbucket.org) repositories. Uses [Bitbucket's API](https://confluence.atlassian.com/display/BITBUCKET/Using+the+Bitbucket+REST+APIs).
Inspired by [jeroenbegyn's](https://gist.github.com/jeroenbegyn) [Bitbucket followers job for Dashing](https://gist.github.com/jeroenbegyn/5385092). Also it uses [vongrippen's](https://github.com/vongrippen) [BitBucketAPI](https://github.com/vongrippen/bitbucket), thanks for this!

# Example

Check this screenshot:

![Screenshot](https://cloud.githubusercontent.com/assets/5159398/5564149/869c1d3a-8eac-11e4-8bc2-5723dc54058b.png)

##Usage

To use this widget put the `bitbucket_commit_count_year.rb` file in your `/jobs` folder.

To include the widget in a dashboard, add the following snippets to the dashboard layout file:
    
    <li data-row="1" data-col="2" data-sizex="1" data-sizey="1">
      <div data-id="bitbucket_commit_count_year" data-view="Number" data-title="Bitbucket commits this year"></div>
    </li>

##Settings

You'll need to add the Bitbucket username or the team name you want to count the commits of. Also you need to pass a username and a password since I am not able to getting the oauth stuff work... The year filter is a simple "starts with" check, so theoretically you can commits per month or day, too.

The commits are fetched every 5 minutes, but you can change that by editing the job schedule.

##Advanced

Use [DashingLongNumberWidget](https://github.com/SocialbitGmbH/DashingLongNumberWidget) if you dont want `1000` commits displayed as `1K`.

Example:

    <li data-row="1" data-col="2" data-sizex="1" data-sizey="1">
      <div data-id="bitbucket_commit_count_year" data-view="Longnumber" data-title="Bitbucket commits this year"></div>
    </li>


## License  
    Copyright 2014 Socialbit GmbH

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.   
