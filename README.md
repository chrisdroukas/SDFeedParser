![SDFeedParser](https://dl.dropboxusercontent.com/s/5gvds2nhdjm6avd/sdfeedparser.png)

SDFeedParser
============

Objective-C parser for the JSON API (https://wordpress.org/plugins/json-api/) plugin for Wordpress


## Installation
1. To install this library, simply copy the 'SDFeedParser' folder into your project, and import it using:

		#import "SDFeedParser.h"

2. You will also need AFNetworking in order to use this library. You can find it here: https://github.com/AFNetworking/AFNetworking

## Installation with CocoaPods

CocoaPods is a dependency manager for Objective-C, which automates and simplifies the process of using 3rd-party libraries like SDFeedParser in your projects. See the "[Getting Started](http://guides.cocoapods.org/syntax/podfile.html)" guide for more information.

### Podfile

        platform :ios, '7.0'
        pod "SDFeedParser", "~> "0.1"


## How to use
       SDFeedParser *parser = [[SDFeedParser alloc]init];
       [parser parseWithURL:@"http://yourblogURL.com/?json=1" withCompletion:^(NSArray *postsArray) {
                NSLog(@"%@", postsArray);
        }];


## Available properties
**SDPost:**

        @property (nonatomic) NSInteger ID;
        @property (nonatomic) NSString *URL;
        @property (nonatomic) NSString *slug;
        @property (nonatomic) NSString *title;
        @property (nonatomic) NSString *plainTitle;
        @property (nonatomic) NSString *thumbnailURL;
        @property (nonatomic) NSString *status;
        @property (nonatomic) NSString *content;
        @property (nonatomic) NSString *plainContent;
        @property (nonatomic) NSInteger contentReadingMinutes;
        @property (nonatomic) NSString *excerpt;
        @property (nonatomic) NSString *date;
        @property (nonatomic) NSString *lastModifiedDate;
        @property (nonatomic) NSArray *categoriesArray;
        @property (nonatomic) NSArray *tagsArray;
        @property (nonatomic) NSDictionary *authorInfo;
        @property (nonatomic) NSArray *commentsArray;
        @property (nonatomic) NSInteger commentsCount;
        @property (nonatomic) NSString *commentsStatus;

**SDComment:**

        @property (nonatomic) NSInteger ID;
        @property (nonatomic) NSString *name;
        @property (nonatomic) NSString *url;
        @property (nonatomic) NSString *date;
        @property (nonatomic) NSString *content;
        @property (nonatomic) NSInteger parent;

**SDCategory:**

        @property (nonatomic) NSInteger ID;
        @property (nonatomic) NSString *slug;
        @property (nonatomic) NSString *title;
        @property (nonatomic) NSString *description;
        @property (nonatomic) NSInteger parent;
        @property (nonatomic) NSInteger postsCount;


**SDTag:**

        @property (nonatomic) NSInteger ID;
        @property (nonatomic) NSString *slug;
        @property (nonatomic) NSString *title;
        @property (nonatomic) NSString *description;
        @property (nonatomic) NSInteger postsCount;



##License

Usage is provided under the [MIT License](http://http//opensource.org/licenses/mit-license.php). See LICENSE for the full details.

