# Calculator
 Just simple Calculator applictaion by js,css and html.With **basic addition, subtraction, multiplication and division functions**.

## Design ideas

First look at what our calculator looks like:

![calculator](https://github.com/shubonnsei/Calculator/blob/main/calculaorJS.png)


Based on this, the following is the design idea, why we should write JS like this.

1. start

2. Users use our web-based computer. Open the page, which corresponds to our action of initializing the calculator (`init` function) -> set the event listener of the button at the same time (response to the event of the user clicking the button)

3. Next the user clicks the button. As shown in the figure above, our calculator has two buttons, one is numbers, and the other is operation symbols, clearing symbols, etc. Here we need to set two functions to respond. Write an if to determine the type of user button, and then based on the result:

    - Is it a number? -> call `handleNumber`
    - Is it a symbol? -> call `handleSymbol`

4. ```
    handleNumber
    - Add numbers to `buffer`
    - update display
    ```

  

5. ```
    handleSymbol
      
    - Depending on the type of symbol, perform the appropriate action, such as clearing, computing a result, deleting a number, or calling `handleMath`
    ```

   

6. ```
    handleMath
      
    - If there are pending operations, call `flushOperation` to execute
    - set `previousOperator` to the current symbol
    ```

   

6. ```
   handleMath
   
   - 如果有待处理的运算，调用 `flushOperation` 执行
   - 设置 `previousOperator` 为当前符号
   ```

   

7. ```
   flushOperation
   
   - 根据 `previousOperator` 执行相应的数学运算
   ```

   

8. 结束

