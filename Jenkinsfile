node {
    stage 'configure'
        def archiveUrl = 'http://api.gbif.org/v1/occurrence/download/request/0000381-150615163101818.zip'

    stage 'import'
        sh "wget --quiet https://raw.githubusercontent.com/gimmefreshdata/archive-importer/master/archives.groovy -O archives.groovy"
        archives = load 'archives.groovy'
        archives.importIfChanged(archiveUrl)
}
