Twitter-Reverse-Auth
====================

Twitter Reverse Auth made easy with a single method!

Open SecretKeys.h and add your Token and Token Secret

Simply include TwitterHelper.h and use the following method:

    [TwitterHelper getCredentialsForAccount:self.userAccount completion:^(NSDictionary *credentials, NSError *error) {
        if (!error && credentials) {
            // Send these credentials to your server
        } else {
            // Something went wrong! Handle it!
            NSLog(@"Reverse Auth process failed. Error returned was: %@\n", [error localizedDescription]);
        }
    }];

Be sure to import all files into your project. This class uses AFNetworking. 
