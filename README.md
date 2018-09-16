# learning

## Understanding Async/Await

A great explaination of Async:  https://stackabuse.com/python-async-await-tutorial/



A great explaination of await: https://www.aeracode.org/2018/02/19/python-async-simplified/

"In the asynchronous world, things change around a bit. Everything runs on a central event loop, which is a bit of core code that lets you run several coroutines at once. Coroutines run synchronously until they hit an await and then they pause, give up control to the event loop, and something else can happen.
This means that synchronous and asynchronous functions/callables are different types - you can't just mix and match them. Try to await a sync function and you'll see Python complain, forget to await an async function and you'll get back a coroutine object rather than the result you wanted.
You actually don't need to know the fine details of how it all works to use it - just know that coroutines have to explicitly give up control via an await. This is different to threads or greenlets, which can context-switch at any time.
If you block a coroutine synchronously - maybe you use time.sleep(10) rather than await asyncio.sleep(10) - you don't return control to the event loop, and you'll hold up the entire process and nothing else can happen. On the plus side, nothing else can run while your code is moving through from one await call to the next, making race conditions harder."
