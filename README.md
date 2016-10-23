# nydesign

Thought it would be fun to play around with github internals to make a contributions design.

It was definitely easier than I thought it would be -- just a little help from a bash script I wrote.
I simply committed empty text files.


bash script

number=1

while [ $number -lt 47 ]; do
    
    touch $number.txt
    git add $number.txt
    echo "Please enter git author/committer date (Feb 16 14:00 2037)"
    read author
    echo "GIT_AUTHOR_DATE=$author GIT_COMMITTER_DATE=$author"
    GIT_AUTHOR_DATE=$author GIT_COMMITTER_DATE=$author git commit -m "$number.txt" 
    number=$((number + 1))
done
