# How to get get font family name for extern imported font

In your ViewController or AppDelegate write this method


#pragma mark ::: get Font Family Name
- (void) getFontFamilyName
{
    NSArray *fontFamilies = [UIFont familyNames];
    
    for (int i = 0; i < [fontFamilies count]; i++)
    {
        NSString *fontFamily = [fontFamilies objectAtIndex:i];
        NSArray *fontNames = [UIFont fontNamesForFamilyName:[fontFamilies objectAtIndex:i]];
        NSLog (@"%@: %@", fontFamily, fontNames);
    }
    
     NSLog(@"*****End Font Family Name **********");
}

Follow this call getFontFamilyName method. For instance you write above code into your ViewController so called getFontFamilyName method 
from viewDidLoad like bellow.

- (void)viewDidLoad
{
    [super viewDidLoad];
    NSLog(@"*****Font Family Name **********");
    [self getFontFamilyName];
}
