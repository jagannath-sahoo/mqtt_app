1. To provide shared library for building mqtt using gcc
 gcc main.c -l paho-mqtt3c

2. TO run code coverage test using gcov
 gcc -fprofile-arcs -ftest-coverage main.c -o main -l paho-mqtt3c
 ./main
 gcov main.c
 now open 'main.c.gcov' file
 Execution number means how many times the particular line is executed
 '####' line means those lines are not executed
 # option: 
 -a     :   To view different blocks
 -b     :   Lines executed:90.91% of 22
            Branches executed:100.00% of 2
            Taken at least once:50.00% of 2
            Calls executed:80.00% of 10 

3. Generate HTML report
    lcov tool is required
    lcov --directory . --capture  --output-file main_coverage.info
    genhtml main_coverage.info
    firefox index.html
echo "# mqtt_app" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/jagannath-sahoo/mqtt_app.git
git push -u origin master
