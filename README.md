Two tiny programs, `todo` and `todone`. I like to alias them to `t` and `d`.

One bonus program, `todos_completed`, to see how much you've accomplished! I like to alias them to `c`

Two manage programs, `todo.edit` and `todo.history`

Another tiny program is to support muti todo list, 
for example, you may want a private todolist, but also want have a public todo list which you can share with team.

You can use that as below:
`todo.new "private" "~/todo/private"`

`todo.ls`

`todo.switch "private"`

# Usage #

Here's an example usage with the aliases:

```bash
$ t feed the plants
1. feed the plants
$ t water the cat
1. feed the plants
2. water the cat
$ t
1. feed the plants
2. water the cat
$ t brush the cat
1. feed the plants
2. water the cat
3. brush the cat
$ d cat
!! multiple matches !!
2. water the cat
3. brush the cat
$ d brush
1. feed the plants
2. water the cat
$ d 1
1. water the cat
$ todo.history | tail -5
+ feed the plants; Wed Mar 20 23:49:37 EDT 2013
+ water the cat; Wed Mar 20 23:49:39 EDT 2013
+ brush the cat; Wed Mar 20 23:49:54 EDT 2013
- brush the cat; Wed Mar 20 23:50:37 EDT 2013
- feed the plants; Wed Mar 20 23:50:39 EDT 2013
$ todos_completed -1hour
√ brush the cat
√ feed the plants
$ todo.new "private" "~/todo/private"
$ todo.new "public" "~/todo/public"
$ todo.ls
 private
*public
$ todo.switch "private" 
*private
public
```


The lists are just plain text files, so it's easy to open them up and edit them
by hand whenever that's necessary. 

or you can use todo.edit to open and edit the text directly.



# Installation #

Clone the repo somewhere on your local

```bash
git clone https://github.com/shaoyangyu/todo-bash.git
```

add `source $path/sourceme.sh` in your .bashrc
