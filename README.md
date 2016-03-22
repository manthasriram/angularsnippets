# angularsnippets

## Directives

### Scope binding

use @ when you want to use the actual value passed in the attribute

```
<player-caption playername="Pete Sampras"/>
```

```
/**
 * Directive to display player header
 * Example - display the player photo and the player name
 */
angular.module('sportingserviceApp').directive('playerCaption', function() {
    return {
        restrict: 'E',
        replace: true,
        scope: {
            id: '@',
            playername: '@',
            logoUrl:'@'
        },
        templateUrl: "/scripts/app/portal/common/components/templates/player-caption.html",
        controller: ['$scope', '$http', function($scope, $http) {
            //Controller the player card

        }],
        link: function(scope, iElement, iAttrs, ctrl) {

        }
    };
});
```
