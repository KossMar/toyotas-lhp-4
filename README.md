# toyotas-lhp-4
toyotas-lhp-4

#import <Foundation/Foundation.h>
#import "Car.h"
#import "Toyota.h"

@interface Car : NSObject
    @property NSString *model;
    -(id) initWithModel: (NSString*) model;
    -(id)drive;
    @end

@implementation Car
    -(id) initWithModel: (NSString*) model {
        self = [super init];
        if (self) {
            _model = model;
        }
        return self;
    }
    -(id)drive {
        NSLog(@"I'm driving a(n) %@. Check me out!", [self model]);
    return self;
    }
    @end


@interface Toyota : Car
    @end

@implementation Toyota
    - (id)init
    {
        self = [self initWithModel: @"Prius"];
        return self;
    }
    @end



int main(int argc, const char * argv[]) {
    @autoreleasepool {
   
        Car *myAuto = [[Car alloc] init];
        [myAuto setModel:@"Civic"];
        [myAuto drive];
        
        Car *myOtherAuto = [[Car alloc] initWithModel: @"Model T"];
        [myOtherAuto drive];
        
        Car *nissan = [[Car alloc] initWithModel:@"Rogue"];
        [nissan drive];
        
        Toyota *firstToyota = [[Toyota alloc] init];
        [firstToyota drive];
        
        
        
    }
    return 0;
}
