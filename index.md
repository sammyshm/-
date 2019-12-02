## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/sammyshm/-/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block
package com.Sammyshe;

import com.mysql.jdbc.Driver;

import java.sql.*;

public class JDBCDemo001 {
    public static void main(String[] args){
        try {
            //*载入驱动
            DriverManager.deregisterDriver(new Driver());
            //*建立连接
            Connection root = DriverManager.getConnection("jdbc:mysql://localhost/test1", "root", "123");
            //*创建statement！！！一定要！
            Statement statement = root.createStatement();
            //执行查询
            String sql="select * from user";
            ResultSet resultSet = statement.executeQuery(sql);
            while(resultSet.next()){
                int id=resultSet.getInt("id");
                String user = resultSet.getString("username");
                String pws = resultSet.getString("password");
                //boolean is_vip = resultSet.getBoolean("is_vip");
                System.out.println("id="+id+"user="+user+pws);
            }
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
}


# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/sammyshm/-/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
