# Session in Java

```java

package com.tyler.session;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestMapping;

import javax.servlet.http.HttpSession;

@Controller
public class MainController {
    // Session is set here
    @RequestMapping("/welcome")
    public String index(HttpSession session){
        session.setAttribute("name", "Tyler");
        return "index.jsp";
    }

    // Session is accessed here without declaring a session variable
    @GetMapping("/demo")
    public String demo(){
        return "demo.jsp";
    }
}
```