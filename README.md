# iPhone Calculator

![](https://raw.githubusercontent.com/atabegruslan/iCalc/master/Illustrations/icalc.png)

Project settings: Uncheck size classes to make your app fit properly on the screen. Adjust project's settings under the 'info' tab and disable the default launch view.
			
```
//
//  ViewController.h
//  calc
//
//  Created by Gary on 6/19/15.
//  Copyright (c) 2015 personal. All rights reserved.
//

#import &lt;UIKit/UIKit.h&gt;

int Method;
int SelectNumber;
float RunningTotal;

@interface ViewController : UIViewController
{
    
    IBOutlet UILabel *Screen;
    
}

-(IBAction)Number1:(id)sender;
-(IBAction)Number2:(id)sender;
-(IBAction)Number3:(id)sender;
-(IBAction)Number4:(id)sender;
-(IBAction)Number5:(id)sender;
-(IBAction)Number6:(id)sender;
-(IBAction)Number7:(id)sender;
-(IBAction)Number8:(id)sender;
-(IBAction)Number9:(id)sender;
-(IBAction)Number0:(id)sender;
-(IBAction)Times:(id)sender;
-(IBAction)Divide:(id)sender;
-(IBAction)Subtract:(id)sender;
-(IBAction)Plus:(id)sender;
-(IBAction)Equals:(id)sender;
-(IBAction)AllClear:(id)sender;

@end
```

```
//
//  ViewController.m
//  calc
//
//  Created by Gary on 6/19/15.
//  Copyright (c) 2015 personal. All rights reserved.
//

#import "ViewController.h"

@interface ViewController ()

@end

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
    // Do any additional setup after loading the view, typically from a nib.
}

- (void)didReceiveMemoryWarning {
    [super didReceiveMemoryWarning];
    // Dispose of any resources that can be recreated.
}


-(IBAction)Number1:(id)sender{
    SelectNumber = SelectNumber*10;
    SelectNumber = SelectNumber+1;
    Screen.text = [NSString stringWithFormat:@"%i", SelectNumber];
}
-(IBAction)Number2:(id)sender{
    SelectNumber = SelectNumber*10;
    SelectNumber = SelectNumber+2;
    Screen.text = [NSString stringWithFormat:@"%i", SelectNumber];
}
-(IBAction)Number3:(id)sender{
    SelectNumber = SelectNumber*10;
    SelectNumber = SelectNumber+3;
    Screen.text = [NSString stringWithFormat:@"%i", SelectNumber];
}
-(IBAction)Number4:(id)sender{
    SelectNumber = SelectNumber*10;
    SelectNumber = SelectNumber+4;
    Screen.text = [NSString stringWithFormat:@"%i", SelectNumber];
}
-(IBAction)Number5:(id)sender{
    SelectNumber = SelectNumber*10;
    SelectNumber = SelectNumber+5;
    Screen.text = [NSString stringWithFormat:@"%i", SelectNumber];
}
-(IBAction)Number6:(id)sender{
    SelectNumber = SelectNumber*10;
    SelectNumber = SelectNumber+6;
    Screen.text = [NSString stringWithFormat:@"%i", SelectNumber];
}
-(IBAction)Number7:(id)sender{
    SelectNumber = SelectNumber*10;
    SelectNumber = SelectNumber+7;
    Screen.text = [NSString stringWithFormat:@"%i", SelectNumber];
}
-(IBAction)Number8:(id)sender{
    SelectNumber = SelectNumber*10;
    SelectNumber = SelectNumber+8;
    Screen.text = [NSString stringWithFormat:@"%i", SelectNumber];
}
-(IBAction)Number9:(id)sender{
    SelectNumber = SelectNumber*10;
    SelectNumber = SelectNumber+9;
    Screen.text = [NSString stringWithFormat:@"%i", SelectNumber];
}
-(IBAction)Number0:(id)sender{
    SelectNumber = SelectNumber*10;
    SelectNumber = SelectNumber+0;
    Screen.text = [NSString stringWithFormat:@"%i", SelectNumber];
}
-(IBAction)Times:(id)sender{
    if(RunningTotal == 0){
        RunningTotal = SelectNumber;
    }else{
        switch(Method){
            case 1:
                RunningTotal = RunningTotal*SelectNumber;
                break;
            case 2:
                RunningTotal = RunningTotal/SelectNumber;
                break;
            case 3:
                RunningTotal = RunningTotal-SelectNumber;
                break;
            case 4:
                RunningTotal = RunningTotal+SelectNumber;
                break;
            default:
                break;
        }
    }
    Method = 1;
    SelectNumber = 0;
    
}
-(IBAction)Divide:(id)sender{
    if(RunningTotal == 0){
        RunningTotal = SelectNumber;
    }else{
        switch(Method){
            case 1:
                RunningTotal = RunningTotal*SelectNumber;
                break;
            case 2:
                RunningTotal = RunningTotal/SelectNumber;
                break;
            case 3:
                RunningTotal = RunningTotal-SelectNumber;
                break;
            case 4:
                RunningTotal = RunningTotal+SelectNumber;
                break;
            default:
                break;
        }
    }
    Method = 2;
    SelectNumber = 0;
}
-(IBAction)Subtract:(id)sender{
    if(RunningTotal == 0){
        RunningTotal = SelectNumber;
    }else{
        switch(Method){
            case 1:
                RunningTotal = RunningTotal*SelectNumber;
                break;
            case 2:
                RunningTotal = RunningTotal/SelectNumber;
                break;
            case 3:
                RunningTotal = RunningTotal-SelectNumber;
                break;
            case 4:
                RunningTotal = RunningTotal+SelectNumber;
                break;
            default:
                break;
        }
    }
    Method = 3;
    SelectNumber = 0;
}
-(IBAction)Plus:(id)sender{
    if(RunningTotal == 0){
        RunningTotal = SelectNumber;
    }else{
        switch(Method){
            case 1:
                RunningTotal = RunningTotal*SelectNumber;
                break;
            case 2:
                RunningTotal = RunningTotal/SelectNumber;
                break;
            case 3:
                RunningTotal = RunningTotal-SelectNumber;
                break;
            case 4:
                RunningTotal = RunningTotal+SelectNumber;
                break;
            default:
                break;
        }
    }
    Method = 4;
    SelectNumber = 0;
}
-(IBAction)Equals:(id)sender{
    if(RunningTotal == 0){
        RunningTotal = SelectNumber;
    }else{
        switch(Method){
            case 1:
                RunningTotal = RunningTotal*SelectNumber;
                break;
            case 2:
                RunningTotal = RunningTotal/SelectNumber;
                break;
            case 3:
                RunningTotal = RunningTotal-SelectNumber;
                break;
            case 4:
                RunningTotal = RunningTotal+SelectNumber;
                break;
            default:
                break;
        }
    }
    Method = 0;
    SelectNumber = 0;
    Screen.text = [NSString stringWithFormat:@"%.2f", RunningTotal];
}
-(IBAction)AllClear:(id)sender{
    Method = 0;
    RunningTotal = 0;
    SelectNumber = 0;
    Screen.text = [NSString stringWithFormat:@"0"];
}

@end
```
