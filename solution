class Command
  def self.sequence(file = 'lib/dictionary.txt')
    words = File.read(file).split
    dict = words.map do |word|
      # normalize upcase, numbers and special chars
      w = word.downcase.gsub(/\W/,'').gsub(/\d/,'')
      # extract words of 4 chars
      if w&.length >= 4
        w.chars.each_cons(4).map do |x|
          [x.join, word]
        end
      end
    end.compact.flatten(1)#.uniq {|a| a.first}
    # remove duplicates
    dict = dict.group_by(&:first)
               .reject{ |k,v| v.count > 1 }
               .values.flatten(1)
    
    File.open('sequences', 'w') { |f| f.puts dict.transpose[0] }
    File.open('words', 'w') { |f| f.puts dict.transpose[1] }
  end
end




## Execute:
Command.sequence('lib/words.txt')
