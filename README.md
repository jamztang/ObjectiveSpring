# ObjectiveSpring
A sample project for using the Spring animation library in Objective-C
project
http://github.com/Mengto/Spring

Code sample

``` objective-c
#import "ViewController.h"
#import "ObjectiveSpring-Swift.h"

@interface ViewController ()

@property (nonatomic, strong) SpringView *springView;

@end

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
    // Do any additional setup after loading the view, typically from a nib.

    SpringView *springView = [[SpringView alloc] initWithFrame:CGRectMake(100, 100, 100, 100)];
    springView.backgroundColor = [UIColor yellowColor];
    springView.animation = @"pop";
    springView.delay = 1;
    springView.duration = 3;
    springView.autostart = true;
    self.springView = springView;
    [self.view addSubview:springView];
}

// Manually trigger an animation
- (IBAction)animateButtonDidPress:(id)sender {
    [self.springView animate];
}

@end
```
