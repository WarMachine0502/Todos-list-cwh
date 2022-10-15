Run Home Page in the build instead of index.html to run functionality.


Deprectaed code for react-router given on [the website](https://v5.reactrouter.com/web/guides/quick-start).
Code changed in App.js from

<Switch>
    <Route exact path="/" render={()=>{
        return(
        <>
        <AddTodo addTodo={addTodo} />
        <Todos todos={todos} onDelete={onDelete} /> 
        </>)
        }}> 
    </Route>
    <Route exact path="/about">
        <About />
    </Route> 
</Switch> 

to

<Routes>
    <Route path="/" element={<><AddTodo addTodo={addTodo} /><Todos todos={todos} onDelete={onDelete} /> </>} />
    <Route path="/about" element={<About />} />
</Routes>
