require 'rake/clean'

CLEAN.include '*.aux'
CLEAN.include '*.log'
CLEAN.include '*.out'

task :default => 'poster.pdf'

file 'poster.pdf' => ['poster.tex', 'uoa.tex', 'eth.tex']
CLOBBER.include 'poster.pdf'

rule '.pdf' => '.tex' do |t|
  sh "pdflatex #{t.source}"
end
