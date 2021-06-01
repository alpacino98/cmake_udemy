cmake_minimum_required(VERSION 3.0.0)

#if commands

set(VAR "YES")

if(VAR)
    message("YES")
else()
    message("NO")
endif()

set(VAR)

if(VAR)
    message("YES")
else()
    message("NO")
endif()

set(VAR "")

if(VAR)
    message("YES")
else()
    message("NO")
endif()

set(NAME Alice)

if(DEFINED NAME)
    message("if block")
else()
    message("else block")
endif()

if(DEFINED AGE)
    message("if block")
else()
    message("else block")
endif()

#COMMAND for if command exists
#EXISTS for checking if a file exists

#for-loop example
foreach(X RANGE 100 105)
    message("${X}")
endforeach()

#function command
function(print_detail name_var)
    message("Deneme ${name_var}")
endfunction()

set(name_var "1 2")

print_detail(${name_var})
print_detail(name_var)



