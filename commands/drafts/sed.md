```bash
# Replace only the first occurrence of the word "old" on each line of a file
sed 's/old/new/' file.txt

# Replace every occurrence of the word "old" on each line of a file
sed 's/old/new/g' file.txt

# Replace every occurrence of the word "old" ignoring case differences
sed 's/old/new/gI' file.txt

# Perform the replacement directly in the original file without creating a new one
sed -i 's/old/new/g' file.txt

# Remove all lines that contain a specific pattern
sed '/pattern/d' file.txt

# Display only the lines containing a specific pattern
sed -n '/pattern/p' file.txt

# Replace all occurrences of "a" with "b" only between lines 10 and 20
sed '10,20 s/a/b/g' file.txt

# Replace all occurrences of "a" with "b" only between two matching patterns
sed '/start/,/end/s/a/b/g' file.txt

# Add a new line after every line that matches a specific pattern
sed '/pattern/a\New line content' file.txt

# Insert a new line before every line that matches a specific pattern
sed '/pattern/i\New line content' file.txt

# Surround matched text with brackets using a capture group
sed 's/\(text\)/[\1]/g' file.txt

# Replace a path containing slashes using an alternate delimiter
sed 's#foo/bar#baz/qux#g' file.txt

# Match and replace using a POSIX character class (digits only)
sed 's/[[:digit:]]\+/NUM/g' file.txt

# Replace only if the match occurs at the beginning of a line
sed 's/^ERROR:/⚠️ ERROR:/g' file.txt

# Replace only if the match occurs at the end of a line
sed 's/;$/./' file.txt

# Replace a literal dot (must be escaped because '.' is a wildcard)
sed 's/\.txt/.md/g' file.txt

# Replace a match captured inside group parentheses (escaped in sed regex)
sed 's/\(hello\) world/\1 universe/' file.txt

# Remove everything after the first comma using greedy matching
sed 's/,.*//' file.txt

# Replace a repeated pattern of m to n lowercase letters
sed 's/[a-z]\{3,5\}/WORD/g' file.txt

# Replace multiple different separators using regex grouping
sed 's/[,:;]/ /g' file.txt

# Substitute only the second occurrence of a word on each line
sed 's/foo/bar/2' file.txt

# Remove lines that contain an entire word using word boundaries
sed '/\<word\>/d' file.txt

```