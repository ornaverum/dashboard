<script lang='ts'>
	import ScrollArea from './../lib/components/ui/scroll-area/scroll-area.svelte';
    import * as Card from '$lib/components/ui/card';
    import { Button } from '$lib/components/ui/button';


    // Asana-like timeline feature, for assignments and projects.

    let dates = [
        {
            'date': '2024-10-01',
            'day': 'Monday',
            'month': 'October',
            'year': '2024',
            'events': [
                {
                    'title': 'Event 1',
                    'description': 'Event 1 Description',
                    'time': '10:00 AM',
                    'location': 'Event 1 Location'
                },
                {
                    'title': 'Event 2',
                    'description': 'Event 2 Description',
                    'time': '11:00 AM',
                    'location': 'Event 2 Location'
                }
            ]
        },
        {
            'date': '2024-10-02',
            'day': 'Tuesday',
            'month': 'October',
            'year': '2024',
            'events': [
                {
                    'title': 'Event 3',
                    'description': 'Event 3 Description',
                    'time': '10:00 AM',
                    'location': 'Event 3 Location'
                },
                {
                    'title': 'Event 4',
                    'description': 'Event 4 Description',
                    'time': '11:00 AM',
                    'location': 'Event 4 Location'
                }
            ]
        },
        {
            'date': '2024-10-03',
            'day': 'Wednesday',
            'month': 'October',
            'year': '2024',
            'events': [
                {
                    'title': 'Event 5',
                    'description': 'Event 5 Description',
                    'time': '10:00 AM',
                    'location': 'Event 5 Location'
                },
                {
                    'title': 'Event 6',
                    'description': 'Event 6 Description',
                    'time': '11:00 AM',
                    'location': 'Event 6 Location'
                }
            ]
        }
    ];
    
</script>

<div class='w-3/4 mx-auto my-3'>
    <Card.Root class='w-full'>
        <Card.Header>
            <Card.Title>Card Title</Card.Title>
            <Card.Description>Card Description</Card.Description>
        </Card.Header>
        <Card.Content>
            <p>Card Content</p>
        </Card.Content>
        <Card.Footer>
            <p>Card Footer</p>
        </Card.Footer>
    </Card.Root>

    <div class='w-1/2 rounded-lg'>
        <ScrollArea class='w-full h-64 rounded-lg'>
            <div class='w-full h-full bg-gray-200'>
                <p>Dates</p>
                {#each dates as date}
                    <div class='w-full h-16 bg-gray-300 flex flex-row p-6 space-x-5'>
                        <p>{date.date}</p>
                        <p>{date.day}</p>
                        <p>{date.month}</p>
                        <p>{date.year}</p>
                    </div>
                {/each}
            </div>
        </ScrollArea>
    </div>
</div>
