# Pass the message  in  vinilla js project ]
### this project is  very simple and straightforward. but I can learn something through this project, 

> ####  That,s what I am learning  javascript new sysntax 
1. **submit event**
1. **ClassList add or remove **
1. **If  else condition **
1. ** Settimeout Function **

> ### Project Code ..........


## Html Code Here ...........
```
<body style="background: #95B8D1">

    <div class="container">
        <div class="row">
            <div class="col-lg-6  offset-lg-3">
                <div class="form shadow-sm  bg-light  rounded"    style="margin: 100px 0;  padding: 30px;">
                    <form id="form-box">
                        <div class="input-group">
                            
                            <input type="text"  id="message" class="form-control" placeholder="Enter your value " aria-label="Username"
                                aria-describedby="basic-addon1">
                                
                                <div class="input-group-prepend">
                                    <button type="submit" class="btn btn-danger ">submit</button>
                                </div>
                                
                        </div>
                        <span  style="font-size: 14px; color: red;  display: none;" id="feedback"  >please enter a value to pass</span>
                    </form>
                    <div class="text">
                        <h4  class="text-danger  mt-3 " >Last message submit </h4>
                        <p id="text"  style="font-weight: 700; color: green; font-size: 28px;"></p>
                        
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Optional JavaScript -->
<body> 
```

##  Javascript Code Here 
```

let form = document.getElementById("form-box");

form.addEventListener("submit", function(e){
    e.preventDefault();

    const message = document.getElementById("message");
    const feedback  = document.getElementById("feedback");
    const text = document.getElementById("text")

    if(message.value == ''){
        feedback.classList.add("show")
        message.style.border = "1px solid red "
        setTimeout(() => {
            feedback.classList.remove("show");
            message.style.border = "none"
        }, 5000);
    }else {
        text.textContent = message.value;
        message.value = "";
        
    }
});
```

