
task :default => [ :lint, :export ]

desc "Lint vocab.yml"
task :lintv do
  sh "../mag-utils/bin/lint_vocab vocab.yml", :verbose => false
end

desc "Lint pp.yml"
task :lintpp do
  sh "../mag-utils/bin/lint_pp pp.yml", :verbose => false
end

desc "Lint all"
task :lint => [ :lintv, :lintpp ]

desc "Export vocab to Anki"
task :exportv do
  sh "../mag-utils/bin/export_anki_vocab -o vocabGrEn.csv vocab.yml", :verbose => true
end

desc "Export pp to Anki (forward/GrEn format)"
task :exportpp do
  sh "../mag-utils/bin/export_anki_pp -o ppfGrEn.csv pp.yml", :verbose => true
  sh "../mag-utils/bin/export_anki_pp --incr -o ppiGrEn.csv pp.yml", :verbose => true
end

desc "Export pp to Anki (reverse/EnGr format)"
task :exportppr do
  sh "../mag-utils/bin/export_anki_pp -r -o ppfEnGr.csv pp.yml", :verbose => true
  sh "../mag-utils/bin/export_anki_pp --incr -r -o ppiEnGr.csv pp.yml", :verbose => true
end

desc "Export all"
task :export => [ :exportv, :exportpp, :exportppr ]

