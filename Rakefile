
task :default => [ :lint, :export ]

desc "Lint vocab.yml"
task :lint do
  sh "../mag-utils/bin/lint_vocab vocab.yml", :verbose => false
  sh "../mag-utils/bin/lint_pp pp.yml", :verbose => false
end

desc "Export to Anki"
task :export do
  sh "../mag-utils/bin/export_to_anki -o vocabGrEn.csv vocab.yml", :verbose => true
end

