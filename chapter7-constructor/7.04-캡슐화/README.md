```javascript
function Rectagle(w, h) {

        var width = w;
        var height = h;  
        

        //메서드 선언
        this.getWidth = function () {
            return width;
        }  
        

        this.getHeight = function () {
            return height;
        }  
        

        this.setWidth = function (w) {
            if(w <0) {
                throw "길이는 음수일 수 없습니다.";
            }else
                width = w;
        }  
        

        this.setHeight = function (h) {
            if(h<0) {
                throw "길이는 음수일 수 없습니다.";
            }else
                height = h;
        }  
        

        Rectangle.prototype.getArea = function () {
            return this.getWidth() * this.getHeight();
        }  
        
        var rectagle = new Rectangle(5, 7);
        
        alert("AREA: "+rectagle.getArea());
    }
```