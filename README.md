# HUYA
Test

判断单前页面是否最前面

var hiddenProperty = 'hidden' in document ? 'hidden' :    
    'webkitHidden' in document ? 'webkitHidden' :    
    'mozHidden' in document ? 'mozHidden' :    
    null;
var visibilityChangeEvent = hiddenProperty.replace(/hidden/i, 'visibilitychange');
var onVisibilityChange = function(){
    if (!document[hiddenProperty]) {    
        console.log('页面激活');
    }else{
        console.log('页面非激活')
    }
}
document.addEventListener(visibilityChangeEvent, onVisibilityChange);
