<script lang="ts">
    import { IconChevronDown, IconCalendarBolt, IconTimelineEvent, IconLinkPlus, IconTableExport } from '@tabler/icons-svelte';
    import { Accordion } from '@skeletonlabs/skeleton-svelte';
	import { slide } from 'svelte/transition';
    import { base } from '$app/paths';

    const features = [
		{
			id: '0',
			title: 'Structured provenance data',
			description:
				'Record ownership events with precise, standardized dates, including uncertain or partial ones, using the Extended Date/Time Format (EDTF) specification, so "circa 1900" or "before 1930" stay structured, meaningful data instead of loose text.',
            fileName: 'feature0.mp4',
			fileType: 'video',
			icon: IconCalendarBolt
                
		},
		{
			id: '1',
			title: 'Visualize provenance timelines',
			description:
				"See an object's full history as a clear timeline, making ownership gaps, transfers, and disputed periods immediately visible.",
            fileName: 'feature1.png',
			fileType: 'image',
			icon: IconTimelineEvent
		},
		{
			id: '2',
			title: 'Source and evidence linking',
			description:
				"Attach documents, archival records, and citations to each event in an object's history, so every claim in the timeline is backed by traceable evidence.",
            fileName: 'feature2.png',
			fileType: 'image',
			icon: IconLinkPlus
		},
        {
			id: '3',
			title: 'Structured data export',
			description:
				"Export your provenance research in structured formats, ready to feed into publications, restitution claims, or other research and collection systems.",
            fileName: 'feature3.png',
			fileType: 'image',
			icon: IconTableExport
		}
	];

    let selected = $state(features[0].id);
</script>


<section class="container mx-auto py-48 px-16 grid grid-cols-12 gap-16">

	<div class="col-span-12 lg:col-span-7">
		{#if features[parseInt(selected)].fileType === 'video'}
			{#key selected}
			<video 
				autoplay disablepictureinpicture loop muted
				class="hidden lg:inline rounded-xl border-1 border-surface-100 aspect-5/4 object-cover"
        	>
				<source src={`${base}/imgs/${features[parseInt(selected)].fileName}`} type="video/mp4" />
			</video>
			{/key}
		{:else if features[parseInt(selected)].fileType === 'image'}
			<img 
            	src={`${base}/imgs/${features[parseInt(selected)].fileName}`}
            	alt={features[parseInt(selected)].title}
				class="hidden lg:inline rounded-xl border-1 border-surface-100"
        	>
		{/if}
    </div>
    
    <div class="col-span-12 lg:col-span-5 flex flex-col gap-16 lg:pl-48">
    <Accordion value={[selected]} onValueChange={(details) => (selected = details.value[0])} class='gap-8'>
	    {#each features as feature, i (feature)}
		    
            <Accordion.Item value={feature.id} class='rounded-lg'>
			    <h3>
				    <Accordion.ItemTrigger class="flex items-center gap-12 p-16 lg:py-24 group">
						<div class="btn p-4 rounded-lg h-fit group-data-[state=open]:preset-filled-brand group-data-[state=open]:text-white">
							<feature.icon stroke="1.5" class="size-24" />
						</div>
						<p class="w-full h4 leading-[1.2] tracking-[-0.01em]">{feature.title}</p>
                        <Accordion.ItemIndicator class="group">
						    <IconChevronDown stroke="1.5" class="size-18 transition group-data-[state=open]:rotate-180" />
					    </Accordion.ItemIndicator>
                    </Accordion.ItemTrigger>
			    </h3>
			
                <Accordion.ItemContent class="px-16 pt-0 pb-24">
                    {#snippet element(attributes)}
					    {#if !attributes.hidden}
						    <div {...attributes} transition:slide={{ duration: 150 }}>
								{#if feature.fileType === 'video'}
									<video 
										autoplay disablepictureinpicture loop muted
										class="mb-16 lg:hidden rounded-lg border-1 border-surface-100 aspect-5/4 object-cover"
        							>
										<source src={`${base}/imgs/${feature.fileName}`} type="video/mp4" />
									</video>
								{:else if feature.fileType === 'image'}
									<img 
										class="mb-16 lg:hidden rounded-lg border-1 border-surface-100"
            							src={`${base}/imgs/${feature.fileName}`}
            							alt={feature.title} 
									/>
								{/if}
							    <p class="text-brand-contrast-dark">{feature.description}</p>
						    </div>
					    {/if}
				    {/snippet}
                </Accordion.ItemContent>

		    </Accordion.Item>
	    {/each}
    </Accordion>
    </div>
</section>